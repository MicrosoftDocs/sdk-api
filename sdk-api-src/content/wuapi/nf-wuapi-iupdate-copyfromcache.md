---
UID: NF:wuapi.IUpdate.CopyFromCache
title: IUpdate::CopyFromCache
author: windows-sdk-content
description: Copies the contents of an update to a specified path.
old-location: wua\iupdate_copyfromcache.htm
old-project: Wua_Sdk
ms.assetid: 43af8bb9-0e09-4541-bc2e-fd40be64a980
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: CopyFromCache, CopyFromCache method [Windows Update Agent], CopyFromCache method [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],CopyFromCache method, IUpdate.CopyFromCache, IUpdate::CopyFromCache, wua.iupdate_copyfromcache, wuapi/IUpdate::CopyFromCache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdate.CopyFromCache
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IUpdate::CopyFromCache


## -description


Copies the contents of an update to a specified path.


## -parameters




### -param path [in]

The path of the location where the update contents are to be copied.


### -param toExtractCabFiles [in]

Reserved for future use. 

You must set <i>toExtractCabFiles</i> to <b>VARIANT_TRUE</b> or <b>VARIANT_FALSE</b>.


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

(This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface has been locked down.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_EULAS_DECLINED</b></dt>
</dl>
</td>
<td width="60%">
The Microsoft Software License Terms are not accepted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DM_NOTDOWNLOADED</b></dt>
</dl>
</td>
<td width="60%">
The files are not downloaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_DM_INCORRECTFILEHASH</b></dt>
</dl>
</td>
<td width="60%">
The file hash verification failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COR_E_DIRECTORYNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
A file or directory could not be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_PATHNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
A file or directory could not be located.

</td>
</tr>
</table>
 




## -remarks



 To copy bundled updates, call this method on the individual updates that are bundled in this update.

<div class="alert"><b>Note</b>  We don't recommend or support the use of the <b>IUpdate::CopyFromCache</b> and <a href="https://msdn.microsoft.com/a12f850a-df08-4263-bb66-94c45f7d875e">IUpdate2::CopyToCache</a> methods to move downloaded updates from one computer to another computer. When the Windows Update Agent (WUA) downloads an update, it might only download the portions of the update’s payload that are necessary for a particular client computer. The necessary portions of the update’s payload can often vary from one computer to another computer, even if the computers have similar hardware and software configurations. <b>IUpdate2::CopyToCache</b> only works if the provided files are an exact match for the files that Windows Update would have normally downloaded on that computer; if you called <b>IUpdate::CopyFromCache</b> to obtain the files on a different computer, the files are likely not to match the files that Windows Update would have normally downloaded so <b>IUpdate2::CopyToCache</b> might fail.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

