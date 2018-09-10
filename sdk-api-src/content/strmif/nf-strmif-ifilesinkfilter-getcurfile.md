---
UID: NF:strmif.IFileSinkFilter.GetCurFile
title: IFileSinkFilter::GetCurFile
author: windows-sdk-content
description: The GetCurFile method retrieves the name and media type of the current file.
old-location: dshow\ifilesinkfilter_getcurfile.htm
tech.root: DirectShow
ms.assetid: 1d635dfc-a3b3-4f75-8356-534a32156686
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetCurFile, GetCurFile method [DirectShow], GetCurFile method [DirectShow],IFileSinkFilter interface, IFileSinkFilter interface [DirectShow],GetCurFile method, IFileSinkFilter.GetCurFile, IFileSinkFilter::GetCurFile, IFileSinkFilterGetCurFile, dshow.ifilesinkfilter_getcurfile, strmif/IFileSinkFilter::GetCurFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
 - IFileSinkFilter.GetCurFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSinkFilter::GetCurFile


## -description



The <code>GetCurFile</code> method retrieves the name and media type of the current file.




## -parameters




### -param ppszFileName [out]

Address of a pointer that receives the name of the file, as an <b>OLESTR</b> type.


### -param pmt [out]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that receives the media type. This parameter can by <b>NULL</b>, in which case the method does not return the media type.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
No file is opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument in <i>ppszFileName</i>.

</td>
</tr>
</table>
 




## -remarks



If the filter has not opened a file, the method might succeed but return <b>NULL</b> in the <i>ppszFileName</i> parameter. Check the value when the method returns.

The method allocates the memory for the string returned in <i>ppszFileName</i>, and the memory for the format block in the media type (if any). The caller must free them by calling <b>CoTaskMemFree</b>. For the media type, you can use the <a href="https://msdn.microsoft.com/b7ec335e-518d-4aa6-8cde-8cb92184d0b0">FreeMediaType</a> function in the base class library.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/aa1d3f8e-9790-4442-ba7e-896981bf1b96">IFileSinkFilter Interface</a>
 

 

