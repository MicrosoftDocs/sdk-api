---
UID: NF:mfapi.MFUnwrapMediaType
title: MFUnwrapMediaType function
author: windows-sdk-content
description: Retrieves a media type that was wrapped in another media type by the MFWrapMediaType function.
old-location: mf\mfunwrapmediatype.htm
tech.root: MedFound
ms.assetid: 2cb6a5ae-315f-4de2-8817-da9d41db14b8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 2cb6a5ae-315f-4de2-8817-da9d41db14b8, MFUnwrapMediaType, MFUnwrapMediaType function [Media Foundation], mf.mfunwrapmediatype, mfapi/MFUnwrapMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
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
 - MFUnwrapMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFUnwrapMediaType function


## -description


Retrieves a media type that was wrapped in another media type by the <a href="https://msdn.microsoft.com/a3dd74bc-1f1c-40b9-a43e-d45ff621248f">MFWrapMediaType</a> function.
        


## -parameters




### -param pWrap

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type that was retrieved by <a href="https://msdn.microsoft.com/a3dd74bc-1f1c-40b9-a43e-d45ff621248f">MFWrapMediaType</a>.
          


### -param ppOrig

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the original media type. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

