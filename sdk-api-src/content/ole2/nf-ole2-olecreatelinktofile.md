---
UID: NF:ole2.OleCreateLinkToFile
title: OleCreateLinkToFile function
author: windows-sdk-content
description: Creates an object that is linked to a file.
old-location: com\olecreatelinktofile.htm
tech.root: com
ms.assetid: 06b013db-0554-4dbc-b19d-28314fb4fee0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: OleCreateLinkToFile, OleCreateLinkToFile function [COM], _ole_OleCreateLinkToFile, com.olecreatelinktofile, ole2/OleCreateLinkToFile
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
 - OleCreateLinkToFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleCreateLinkToFile function


## -description


Creates an object that is linked to a file.


## -parameters




### -param lpszFileName [in]

Pointer to a string naming the source file to be linked to.


### -param riid [in]

Reference to the identifier of the interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>).


### -param renderopt [in]

Value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. Additional considerations are described in the following Remarks section.


### -param lpFormatEtc [in]

Pointer to a value from the enumeration <a href="https://msdn.microsoft.com/bab871ba-4ec4-49fd-854a-585732b91290">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>pFormatEtc</i> parameter.


### -param pClientSite [in]

Pointer to an instance of <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.


### -param pStg [in]

 Pointer to the <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object. This parameter cannot be <b>NULL</b>.


### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.


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
<dt><b>STG_E_FILENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The file name is invalid.

</td>
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



The <b>OleCreateLinkToFile</b> function differs from the <a href="https://msdn.microsoft.com/ef52dc37-aa63-47f3-a04f-f9d22178690f">OleCreateLink</a> function because it can create links both to files that are not aware of OLE, as well as to those that are using the Windows Packager.




## -see-also




<a href="https://msdn.microsoft.com/ef52dc37-aa63-47f3-a04f-f9d22178690f">OleCreateLink</a>
 

 

