---
UID: NF:wuapi.IUpdate2.CopyToCache
title: IUpdate2::CopyToCache (wuapi.h)
description: Copies files for an update from a specified source location to the internal Windows Update Agent (WUA) download cache.
helpviewer_keywords: ["CopyToCache","CopyToCache method [Windows Update Agent]","CopyToCache method [Windows Update Agent]","IUpdate2 interface","IUpdate2 interface [Windows Update Agent]","CopyToCache method","IUpdate2.CopyToCache","IUpdate2::CopyToCache","wua.iupdate2_copytocache","wuapi/IUpdate2::CopyToCache"]
old-location: wua\iupdate2_copytocache.htm
tech.root: wua
ms.assetid: a12f850a-df08-4263-bb66-94c45f7d875e
ms.date: 12/05/2018
ms.keywords: CopyToCache, CopyToCache method [Windows Update Agent], CopyToCache method [Windows Update Agent],IUpdate2 interface, IUpdate2 interface [Windows Update Agent],CopyToCache method, IUpdate2.CopyToCache, IUpdate2::CopyToCache, wua.iupdate2_copytocache, wuapi/IUpdate2::CopyToCache
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate2::CopyToCache
 - wuapi/IUpdate2::CopyToCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate2.CopyToCache
---

# IUpdate2::CopyToCache


## -description

Copies files for an update from a specified source location to the internal Windows Update Agent (WUA) download cache.

## -parameters

### -param pFiles [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-istringcollection">IStringCollection</a> interface that represents a collection of strings that contain the full paths of the files for an update.   

The strings  must give the full paths of the files that are being copied. The strings cannot give only the directory that contains the files.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer could not access the update site.

</td>
</tr>
</table>

## -remarks

This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface has been locked down.

<div class="alert"><b>Note</b>  We don't recommend or support the use of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-copyfromcache">IUpdate::CopyFromCache</a> and <b>IUpdate2::CopyToCache</b> methods to move downloaded updates from one computer to another computer. When the Windows Update Agent (WUA) downloads an update, it might only download the portions of the update’s payload that are necessary for a particular client computer. The necessary portions of the update’s payload can often vary from one computer to another computer, even if the computers have similar hardware and software configurations. <b>IUpdate2::CopyToCache</b> only works if the provided files are an exact match for the files that Windows Update would have normally downloaded on that computer; if you called <b>IUpdate::CopyFromCache</b> to obtain the files on a different computer, the files are likely not to match the files that Windows Update would have normally downloaded so <b>IUpdate2::CopyToCache</b> might fail.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate2">IUpdate2</a>