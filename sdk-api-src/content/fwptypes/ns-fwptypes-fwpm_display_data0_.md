---
UID: NS:fwptypes.FWPM_DISPLAY_DATA0_
title: FWPM_DISPLAY_DATA0_
author: windows-sdk-content
description: The FWPM_DISPLAY_DATA0 structure specifies a name and description for a layer, a filter, a provider, a provider context, a callout, or an open session.Note  FWPM_DISPLAY_DATA0 is a specific version of FWPM_DISPLAY_DATA.
old-location: netvista\fwpm_display_data0.htm
tech.root: NetVista
ms.assetid: dfd92824-feea-4f57-ba2f-b2d56dee48ad
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWPM_DISPLAY_DATA0, FWPM_DISPLAY_DATA0 structure [Network Drivers Starting with Windows Vista], FWPM_DISPLAY_DATA0_, fwptypes/FWPM_DISPLAY_DATA0, netvista.fwpm_display_data0, wfp_ref_3_struct_2_fwpm_A-Z_8ccfd63b-e507-4065-904f-9887c8695b0d.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwptypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows Vista.
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWPM_DISPLAY_DATA0
product: Windows
targetos: Windows
req.typenames: FWPM_DISPLAY_DATA0
req.redist: 
---

# FWPM_DISPLAY_DATA0_ structure


## -description


The <b>FWPM_DISPLAY_DATA0</b> structure specifies a name and description for a layer, a filter, a provider,
  a provider context, a callout, or an open session.
<div class="alert"><b>Note</b>  <b>FWPM_DISPLAY_DATA0</b> is a specific version of <b>FWPM_DISPLAY_DATA</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field name

A pointer to a NULL-terminated string that specifies the name to be associated with the layer,
     filter, provider, provider context, callout, or open session. This can be either a literal string or an
     indirect string.


### -field description

A pointer to a NULL-terminated string that specifies the description to be associated with the
     layer, filter, provider, provider context, callout, or open session. This can be either a literal string
     or an indirect string.


## -remarks



For Multilingual User Interface (MUI) support, the 
    <b>Name</b> and 
    <b>Description</b> members can be pointers to indirect strings. If a string is an indirect string, it is
    in this form.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>@filename,resource</pre>
</td>
</tr>
</table></span></div>
The target string is located in the specified file. The resource value identifies the specific string
    within the file. If the resource value is zero or greater, the number is used as an index of the string
    in a binary file. If the resource value is negative, it is used as a resource identifier in a resource
    file.

An FWPM_DISPLAY_DATA0 structure is contained within the 
    <a href="https://msdn.microsoft.com/a6f19d6d-4fce-4774-86c1-10d1bf77315f">FWPM_CALLOUT0</a> and 
    <a href="https://msdn.microsoft.com/971faf9c-2847-4829-ae96-b9fde15f5c26">FWPM_SESSION0</a> structures.

An FWPM_DISPLAY_DATA0 structure is also contained within the <a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a>, <a href="https://msdn.microsoft.com/77d567a7-9495-4f16-9b02-e44a1ef67022">FWPM_LAYER0</a>,
    <a href="https://msdn.microsoft.com/692714fd-14f1-4f8b-a033-1f30b6d0b95a">FWPM_PROVIDER0</a>, <a href="https://msdn.microsoft.com/99105044-f4fa-42f2-8393-f0ee8948e9ff">FWPM_PROVIDER_CONTEXT0</a>, and <a href="https://msdn.microsoft.com/ce689b1d-1f5c-4dde-96cd-9001de3827aa">FWPM_SUBLAYER0</a> structures. For more information about these
    structures, see the <a href="https://msdn.microsoft.com/0436f559-20e6-4199-8391-10eb7d85df23">Windows Filtering Platform</a> section in the Microsoft Windows SDK documentation.

The 
    <b>Name</b> member is required for all of these structures except for the <a href="https://msdn.microsoft.com/971faf9c-2847-4829-ae96-b9fde15f5c26">FWPM_SESSION0</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/a6f19d6d-4fce-4774-86c1-10d1bf77315f">FWPM_CALLOUT0</a>



<a href="https://msdn.microsoft.com/971faf9c-2847-4829-ae96-b9fde15f5c26">FWPM_SESSION0</a>
 

 

