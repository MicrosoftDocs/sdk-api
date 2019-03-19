---
UID: NF:strmif.IDvdInfo2.GetSubpictureAttributes
title: IDvdInfo2::GetSubpictureAttributes (strmif.h)
author: windows-sdk-content
description: The GetSubpictureAttributes method retrieves the attributes of the specified subpicture stream in the specified title or menu.
old-location: dshow\idvdinfo2_getsubpictureattributes.htm
tech.root: DirectShow
ms.assetid: 3dce0c01-1d39-4f49-984b-8cce08a2e67b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSubpictureAttributes, GetSubpictureAttributes method [DirectShow], GetSubpictureAttributes method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetSubpictureAttributes method, IDvdInfo2.GetSubpictureAttributes, IDvdInfo2::GetSubpictureAttributes, IDvdInfo2GetSubpictureAttributes, dshow.idvdinfo2_getsubpictureattributes, strmif/IDvdInfo2::GetSubpictureAttributes
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetSubpictureAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetSubpictureAttributes


## -description



The <code>GetSubpictureAttributes</code> method retrieves the attributes of the specified subpicture stream in the specified title or menu.




## -parameters




### -param ulStream [in]

Index number, from 0 through 31, of the subpicture stream to query. See Remarks.


### -param pATR [out]

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
<th>Value
            </th>
<th>Description
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
 

 

