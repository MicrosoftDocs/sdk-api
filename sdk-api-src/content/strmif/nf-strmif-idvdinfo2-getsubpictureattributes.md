---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IDvdInfo2::GetSubpictureAttributes


## -description



The <code>GetSubpictureAttributes</code> method retrieves the attributes of the specified subpicture stream in the specified title or menu.




## -parameters




### -param ulStream [in]

Index number, from 0 through 31, of the subpicture stream to query. See Remarks.


### -param pATR






#### - pAttributes [out]

Pointer to a <a href="https://msdn.microsoft.com/55ddfa21-5600-4aa9-b554-7ff7f3c05b91">DVD_SubpictureAttributes</a> structure that receives the subpicture attributes.


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No subpicture streams were found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The subpicture has no defined attributes.

</td>
</tr>
</table>
 




## -remarks



The index numbers 0-31 are valid only for titles. Menus have only one subpicture stream, which must be specified using one of the constants in the table below:

<table>
<tr>
<th>
              Value
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>DVD_STREAM_DATA_CURRENT (0x800)</td>
<td>To query the currently selected subpicture stream.</td>
</tr>
<tr>
<td>DVD_STREAM_DATA_VMGM (0x400)</td>
<td>To query the subpicture attributes for the Video Manager or "Top" Menu.</td>
</tr>
<tr>
<td>DVD_STREAM_DATA_VTSM (0x401)</td>
<td>To query the subpicture attributes for the currently selected Video Title Set Menu.</td>
</tr>
</table>
 

This method is demonstrated in the DVDSample application in <b>CDvdCore::GetSPAttributes()</b> and <b>CSPLangDlg::GetSPLang</b>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>



<a href="https://msdn.microsoft.com/8c5f8072-b74f-4e15-8991-73bcc4145fd2">Working With DVD Menus</a>
 

 

