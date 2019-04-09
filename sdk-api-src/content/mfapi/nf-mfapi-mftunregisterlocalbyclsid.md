---
UID: NF:mfapi.MFTUnregisterLocalByCLSID
title: MFTUnregisterLocalByCLSID function (mfapi.h)
author: windows-sdk-content
description: Unregisters a Media Foundation transform (MFT) from the caller's process.
old-location: mf\mftunregisterlocalbyclsid.htm
tech.root: medfound
ms.assetid: ebdf50ad-99cb-4ebf-9050-da0b2d9f26df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFTUnregisterLocalByCLSID, MFTUnregisterLocalByCLSID function [Media Foundation], mf.mftunregisterlocalbyclsid, mfapi/MFTUnregisterLocalByCLSID
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFTUnregisterLocalByCLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFTUnregisterLocalByCLSID function


## -description


Unregisters a Media Foundation transform (MFT) from the caller's process.


## -parameters




### -param clsidMFT [in]

The class identifier (CLSID) of the MFT.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(<b>ERROR_NOT_FOUND</b>)</b></dt>
</dl>
</td>
<td width="60%">
The MFT specified by the <i>clsidMFT</i> parameter was not registered in this process.

</td>
</tr>
</table>
 




## -remarks



Use this function to unregister a local MFT that was previously registered through the <a href="https://msdn.microsoft.com/80c45ac3-4487-41bf-a5f5-f459db3cd700">MFTRegisterLocalByCLSID</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

