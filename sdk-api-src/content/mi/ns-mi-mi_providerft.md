---
UID: NS:mi._MI_ProviderFT
title: MI_ProviderFT (mi.h)
description: A support structure used in the MI_ClassDecl and MI_Module structures.
helpviewer_keywords: ["MI_ProviderFT","MI_ProviderFT structure [Windows Management Infrastructure (MI)]","mi/MI_ProviderFT","wmi_v2.mi_providerft"]
old-location: wmi_v2\mi_providerft.htm
tech.root: wmi_v2
ms.assetid: 494eb3cb-6476-4fe3-8da4-dc7112c6f62f
ms.date: 12/05/2018
ms.keywords: MI_ProviderFT, MI_ProviderFT structure [Windows Management Infrastructure (MI)], mi/MI_ProviderFT, wmi_v2.mi_providerft
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_ProviderFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ProviderFT
 - mi/_MI_ProviderFT
 - MI_ProviderFT
 - mi/MI_ProviderFT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ProviderFT
---

# MI_ProviderFT structure


## -description

A support structure used in the <a href="/windows/desktop/api/mi/ns-mi-mi_classdecl">MI_ClassDecl</a> and <a href="/windows/desktop/api/mi/ns-mi-mi_module">MI_Module</a> structures.

## -struct-fields

### -field Load

The server invokes this function to initialize the provider, which
 performs initialization activities.

### -field Unload

The server invokes this function to release any resources held by the 
 provider.

### -field GetInstance

The server invokes this function to obtain a single CIM 
 instance from the provider.

### -field EnumerateInstances

The server calls this function to enumerate instances of a CIM class 
 in the target namespace.

### -field CreateInstance

The server calls this function to create a single CIM 
 instance in the target namespace.

### -field ModifyInstance

The server calls this function to modify an existing CIM 
 instance in the target namespace. The instance must already exist.

### -field DeleteInstance

The server calls this function to delete a single CIM 
 instance from the target namespace.

### -field AssociatorInstances

The server calls this function to find all CIM instances
 associated with a particular 'source' CIM instance.

### -field ReferenceInstances

The server calls this function to enumerate association 
 instances that refer to a particular CIM instance.

### -field EnableIndications

The server calls this function to enable indications delivery 
 from the provider.

### -field DisableIndications

The server calls this function to disable indications delivery 
 from the provider.

### -field Subscribe

The server invokes this function to subscribe to indications.

### -field Unsubscribe

The server invokes this function to unsubscribe from indications.

### -field Invoke

The server calls this function to carry out a CIM extrinsic method 
 invocation on behalf of a requestor.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dn759647(v=vs.85)">MI_ProviderFT_AssociatorInstances</a>



<a href="/previous-versions/windows/desktop/legacy/dn759648(v=vs.85)">MI_ProviderFT_CreateInstance</a>



<a href="/previous-versions/windows/desktop/legacy/dn759649(v=vs.85)">MI_ProviderFT_DeleteInstance</a>



<a href="/previous-versions/windows/desktop/legacy/dn759650(v=vs.85)">MI_ProviderFT_DisableIndications</a>



<a href="/previous-versions/windows/desktop/legacy/dn759651(v=vs.85)">MI_ProviderFT_EnableIndications</a>



<a href="/previous-versions/windows/desktop/legacy/dn759652(v=vs.85)">MI_ProviderFT_EnumerateInstances</a>



<a href="/previous-versions/windows/desktop/legacy/dn759653(v=vs.85)">MI_ProviderFT_GetInstance</a>



<a href="/previous-versions/windows/desktop/legacy/dn759654(v=vs.85)">MI_ProviderFT_Invoke</a>



<a href="/previous-versions/windows/desktop/legacy/dn759655(v=vs.85)">MI_ProviderFT_Load</a>



<a href="/previous-versions/windows/desktop/legacy/dn759656(v=vs.85)">MI_ProviderFT_ModifyInstance</a>



<a href="/previous-versions/windows/desktop/legacy/dn759657(v=vs.85)">MI_ProviderFT_ReferenceInstances</a>



<a href="/previous-versions/windows/desktop/legacy/dn759658(v=vs.85)">MI_ProviderFT_Subscribe</a>



<a href="/previous-versions/windows/desktop/legacy/dn759659(v=vs.85)">MI_ProviderFT_Unload</a>



<a href="/previous-versions/windows/desktop/legacy/dn759660(v=vs.85)">MI_ProviderFT_Unsubscribe</a>