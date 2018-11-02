---
UID: NF:mfidl.MFCreateSourceResolver
title: MFCreateSourceResolver function
author: windows-sdk-content
description: Creates the source resolver, which is used to create a media source from a URL or byte stream.
old-location: mf\mfcreatesourceresolver.htm
tech.root: medfound
ms.assetid: 60d6b0e2-5ab2-4a20-99d9-e6b806a1f576
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 60d6b0e2-5ab2-4a20-99d9-e6b806a1f576, MFCreateSourceResolver, MFCreateSourceResolver function [Media Foundation], mf.mfcreatesourceresolver, mfidl/MFCreateSourceResolver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Mf.lib
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
 - MFCreateSourceResolver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateSourceResolver function


## -description


Creates the source resolver, which is used to create a media source from a URL or byte stream.
        


## -parameters




### -param ppISourceResolver [out]

Receives a pointer to the source resolver's <a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from mf.dll. Starting in Windows 7, this function is exported from mfplat.dll, and mf.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Ee663600(v=VS.85).aspx">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>
 

 

