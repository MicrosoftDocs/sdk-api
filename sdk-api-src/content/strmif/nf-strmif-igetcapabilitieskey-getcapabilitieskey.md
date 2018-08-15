---
UID: NF:strmif.IGetCapabilitiesKey.GetCapabilitiesKey
title: IGetCapabilitiesKey::GetCapabilitiesKey
author: windows-sdk-content
description: The GetCapabilitiesKey method gets a registry key that contains capability information for the codec.
old-location: dshow\igetcapabilitieskey_getcapabilitieskey.htm
old-project: DirectShow
ms.assetid: 02c3edfe-9ce1-4d9f-bdd1-79e818b43800
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetCapabilitiesKey, GetCapabilitiesKey method [DirectShow], GetCapabilitiesKey method [DirectShow],IGetCapabilitiesKey interface, IGetCapabilitiesKey interface [DirectShow],GetCapabilitiesKey method, IGetCapabilitiesKey.GetCapabilitiesKey, IGetCapabilitiesKey::GetCapabilitiesKey, IGetCapabilitiesKeyGetCapabiltitiesKey, dshow.igetcapabilitieskey_getcapabilitieskey, strmif/IGetCapabilitiesKey::GetCapabilitiesKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGetCapabilitiesKey.GetCapabilitiesKey
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGetCapabilitiesKey::GetCapabilitiesKey


## -description



The <b>GetCapabilitiesKey</b> method gets a registry key that contains capability information for the codec.




## -parameters




### -param pHKey






#### - pKey [out]

Receives a handle to the registry key. The caller must close the handle by calling <b>RegCloseKey</b>.
          


## -returns



This method can return one of these values.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
There is no capabilities key for this codec.

</td>
</tr>
</table>
 




## -remarks



To enumerate the values for the returned key, call <b>RegEnumValue</b>.




## -see-also




<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/97a9112f-7b7b-4a7e-8f40-bdb148d413c8">IGetCapabilitiesKey</a>
 

 

