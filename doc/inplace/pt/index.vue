<template>
    <div class="doc-main">
        <div class="doc-intro">
            <h1>Inplace Pass Through</h1>
        </div>
        <DocSections :docs="docs" />
    </div>
    <DocSectionNav :docs="docs" />
</template>

<script>
import DocApiTable from '@/components/doc/DocApiTable.vue';
import { getPTOption } from '@/components/doc/helpers/PTHelper.js';
import PtDoc from './PTDoc.vue';
import PTImage from './PTImage.vue';

export default {
    data() {
        return {
            docs: [
                {
                    id: 'pt.image',
                    label: 'Wireframe',
                    component: PTImage
                },
                {
                    id: 'pt.doc.badge',
                    label: 'Inplace PT Options',
                    component: DocApiTable,
                    data: getPTOption('Inplace')
                },
                {
                    id: 'pt.demo',
                    label: 'Demo',
                    component: PtDoc
                }
            ]
        };
    }
};
</script>
