---
UID: NF:mfidl.IMFMediaTypeHandler.GetCurrentMediaType
title: IMFMediaTypeHandler::GetCurrentMediaType
author: windows-sdk-content
description: Retrieves the current media type of the object.
old-location: mf\imfmediatypehandler_getcurrentmediatype.htm
tech.root: medfound
ms.assetid: b1676e40-81a2-4311-bba6-528bfa45a708
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetCurrentMediaType, GetCurrentMediaType method [Media Foundation], GetCurrentMediaType method [Media Foundation],IMFMediaTypeHandler interface, IMFMediaTypeHandler interface [Media Foundation],GetCurrentMediaType method, IMFMediaTypeHandler.GetCurrentMediaType, IMFMediaTypeHandler::GetCurrentMediaType, b1676e40-81a2-4311-bba6-528bfa45a708, mf.imfmediatypehandler_getcurrentmediatype, mfidl/IMFMediaTypeHandler::GetCurrentMediaType
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
 - IMFMediaTypeHandler.GetCurrentMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaTypeHandler::GetCurrentMediaType


## -description



Retrieves the current media type of the object.




## -parameters




### -param ppMediaType [out]

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
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
No media type is set.
              

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a>
 

 

