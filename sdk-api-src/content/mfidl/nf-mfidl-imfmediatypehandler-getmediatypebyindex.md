---
UID: NF:mfidl.IMFMediaTypeHandler.GetMediaTypeByIndex
title: IMFMediaTypeHandler::GetMediaTypeByIndex
author: windows-sdk-content
description: Retrieves a media type from the object's list of supported media types.
old-location: mf\imfmediatypehandler_getmediatypebyindex.htm
tech.root: medfound
ms.assetid: a1827675-bbc4-45d8-8c6e-644b0d2addd4
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetMediaTypeByIndex, GetMediaTypeByIndex method [Media Foundation], GetMediaTypeByIndex method [Media Foundation],IMFMediaTypeHandler interface, IMFMediaTypeHandler interface [Media Foundation],GetMediaTypeByIndex method, IMFMediaTypeHandler.GetMediaTypeByIndex, IMFMediaTypeHandler::GetMediaTypeByIndex, a1827675-bbc4-45d8-8c6e-644b0d2addd4, mf.imfmediatypehandler_getmediatypebyindex, mfidl/IMFMediaTypeHandler::GetMediaTypeByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaTypeHandler.GetMediaTypeByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaTypeHandler::GetMediaTypeByIndex


## -description



Retrieves a media type from the object's list of supported media types.




## -parameters




### -param dwIndex [in]

Zero-based index of the media type to retrieve. To get the number of media types in the list, call <a href="https://msdn.microsoft.com/c5ee41bc-ee8b-4990-ae9d-92ef54597f31">IMFMediaTypeHandler::GetMediaTypeCount</a>.
          


### -param ppType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The caller must release the interface.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwIndex</i> parameter is out of range.
              

</td>
</tr>
</table>
 




## -remarks



Media types are returned in the approximate order of preference. The list of supported types is not guaranteed to be complete. To test whether a particular media type is supported, call <a href="https://msdn.microsoft.com/ea52defa-8b78-4f40-97ae-ed6a5ee4849e">IMFMediaTypeHandler::IsMediaTypeSupported</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a>
 

 

