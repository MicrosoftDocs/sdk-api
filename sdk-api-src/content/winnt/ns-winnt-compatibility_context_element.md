---
UID: NS:winnt._COMPATIBILITY_CONTEXT_ELEMENT
title: COMPATIBILITY_CONTEXT_ELEMENT (winnt.h)
description: The COMPATIBILITY_CONTEXT_ELEMENT structure is used by the QueryActCtxW function as part of the ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION structure.
helpviewer_keywords: ["*PCOMPATIBILITY_CONTEXT_ELEMENT","COMPATIBILITY_CONTEXT_ELEMENT","COMPATIBILITY_CONTEXT_ELEMENT structure [Setup API]","PCOMPATIBILITY_CONTEXT_ELEMENT","PCOMPATIBILITY_CONTEXT_ELEMENT structure pointer [Setup API]","_COMPATIBILITY_CONTEXT_ELEMENT","setup.compatibility_context_element","winnt/COMPATIBILITY_CONTEXT_ELEMENT","winnt/PCOMPATIBILITY_CONTEXT_ELEMENT"]
old-location: setup\compatibility_context_element.htm
tech.root: setup
ms.assetid: 3e654f44-43f6-4282-b277-14ed6e25abf2
ms.date: 12/05/2018
ms.keywords: '*PCOMPATIBILITY_CONTEXT_ELEMENT, COMPATIBILITY_CONTEXT_ELEMENT, COMPATIBILITY_CONTEXT_ELEMENT structure [Setup API], PCOMPATIBILITY_CONTEXT_ELEMENT, PCOMPATIBILITY_CONTEXT_ELEMENT structure pointer [Setup API], _COMPATIBILITY_CONTEXT_ELEMENT, setup.compatibility_context_element, winnt/COMPATIBILITY_CONTEXT_ELEMENT, winnt/PCOMPATIBILITY_CONTEXT_ELEMENT'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: COMPATIBILITY_CONTEXT_ELEMENT, *PCOMPATIBILITY_CONTEXT_ELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COMPATIBILITY_CONTEXT_ELEMENT
 - winnt/_COMPATIBILITY_CONTEXT_ELEMENT
 - PCOMPATIBILITY_CONTEXT_ELEMENT
 - winnt/PCOMPATIBILITY_CONTEXT_ELEMENT
 - COMPATIBILITY_CONTEXT_ELEMENT
 - winnt/COMPATIBILITY_CONTEXT_ELEMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - COMPATIBILITY_CONTEXT_ELEMENT
---

# COMPATIBILITY_CONTEXT_ELEMENT structure


## -description

The <b>COMPATIBILITY_CONTEXT_ELEMENT</b> structure is used by the <a href="/windows/win32/api/winnt/ns-winnt-activation_context_compatibility_information">QueryActCtxW</a> function as part of the <a href="/windows/desktop/api/winnt/ns-winnt-activation_context_compatibility_information">ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION</a> structure.

## -struct-fields

### -field Id

This is a <b>GUID</b> that specifies a version of  Windows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>{e2011457-1546-43c5-a5fe-008deee3d3f0}</dt>
</dl>
</td>
<td width="60%">
Windows Vista

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</dt>
</dl>
</td>
<td width="60%">
Windows 7

</td>
</tr>
</table>

### -field Type

A value of the <a href="/windows/desktop/api/winnt/ne-winnt-actctx_compatibility_element_type">ACTCTX_COMPATIBILITY_ELEMENT_TYPE</a> enumeration that describes the compatibility elements in the application manifest.