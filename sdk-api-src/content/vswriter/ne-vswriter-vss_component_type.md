---
UID: NE:vswriter.VSS_COMPONENT_TYPE
title: VSS_COMPONENT_TYPE (vswriter.h)
description: Specify the type of component being used with a shadow copy backup operation.
helpviewer_keywords: ["VSS_COMPONENT_TYPE","VSS_COMPONENT_TYPE enumeration [VSS]","VSS_CT_DATABASE","VSS_CT_FILEGROUP","VSS_CT_UNDEFINED","_win32_vss_component_type","base.vss_component_type","enumeration [VSS]","vswriter/VSS_COMPONENT_TYPE","vswriter/VSS_CT_DATABASE","vswriter/VSS_CT_FILEGROUP","vswriter/VSS_CT_UNDEFINED"]
old-location: base\vss_component_type.htm
tech.root: base
ms.assetid: ba3b726c-448a-46c0-8fa5-5793497aa385
ms.date: 12/05/2018
ms.keywords: VSS_COMPONENT_TYPE, VSS_COMPONENT_TYPE enumeration [VSS], VSS_CT_DATABASE, VSS_CT_FILEGROUP, VSS_CT_UNDEFINED, _win32_vss_component_type, base.vss_component_type, enumeration [VSS], vswriter/VSS_COMPONENT_TYPE, vswriter/VSS_CT_DATABASE, vswriter/VSS_CT_FILEGROUP, vswriter/VSS_CT_UNDEFINED
req.header: vswriter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_COMPONENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VSS_COMPONENT_TYPE
 - vswriter/VSS_COMPONENT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_COMPONENT_TYPE
---

# VSS_COMPONENT_TYPE enumeration


## -description

The <b>VSS_COMPONENT_TYPE</b> enumeration is used by both 
    the requester and the writer to specify the type of component being used with a shadow copy backup 
    operation.

## -enum-fields

### -field VSS_CT_UNDEFINED:0

Undefined component type. 
      

This value indicates an application error.

### -field VSS_CT_DATABASE

Database component.

### -field VSS_CT_FILEGROUP

File group component. This is any component other than a database.

## -remarks

A writer sets a component's type when it adds the component to its Writer Metadata Document using 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">IVssCreateWriterMetadata::AddComponent</a>.

Writers and requesters can find the type information of components selected for inclusion in a Backup 
    Components Document through calls to 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getcomponenttype">IVssComponent::GetComponentType</a> to return 
    a component type directly.

A requester can obtain the type of any component in a given writer's Writer Metadata Document by doing the 
    following:

<ol>
<li>Using 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">IVssExamineWriterMetadata::GetComponent</a> 
      to obtain a <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a> interface</li>
<li>Using 
      <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getcomponentinfo">IVssWMComponent::GetComponentInfo</a> to 
      return a <a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> structure</li>
<li>Examining the <b>Type</b> member of the 
      <a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> object</li>
</ol>

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getcomponenttype">IVssComponent::GetComponentType</a>



<a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_source_type">VSS_SOURCE_TYPE</a>
