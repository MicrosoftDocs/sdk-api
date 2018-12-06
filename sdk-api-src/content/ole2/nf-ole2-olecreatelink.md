---
UID: NF:ole2.OleCreateLink
title: OleCreateLink function
author: windows-sdk-content
description: Creates an OLE compound-document linked object.
old-location: com\olecreatelink.htm
tech.root: com
ms.assetid: ef52dc37-aa63-47f3-a04f-f9d22178690f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OleCreateLink, OleCreateLink function [COM], _ole_OleCreateLink, com.olecreatelink, ole2/OleCreateLink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleCreateLink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleCreateLink function


## -description


Creates an OLE compound-document linked object.


## -parameters




### -param pmkLinkSrc [in]

Pointer to the <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a> interface on the moniker that can be used to locate the source of the linked object.


### -param riid [in]

Reference to the identifier of the interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>).


### -param renderopt [in]

Specifies a value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. Additional considerations are described in the Remarks section below.


### -param lpFormatEtc [in]

Pointer to a value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>lpFormatEtc</i> parameter.


### -param pClientSite [in]

Pointer to an instance of <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.


### -param pStg [in]

Pointer to the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object. This parameter cannot be <b>NULL</b>.


### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Not able to bind to source.

</td>
</tr>
</table>
 




## -remarks



Call <b>OleCreateLink</b> to allow a container to create a link to an object.




## -see-also




<a href="https://msdn.microsoft.com/9ca3e997-9a96-43c3-a213-de8c8440cd54">IOleClientSite::GetMoniker</a>



<a href="https://msdn.microsoft.com/1313cd9a-757d-4716-abac-027cff9fee03">IOleObject::SetMoniker</a>
 

 

