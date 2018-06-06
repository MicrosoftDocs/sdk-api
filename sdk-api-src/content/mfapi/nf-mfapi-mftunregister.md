---
UID: NF:mfapi.MFTUnregister
title: MFTUnregister function
author: windows-sdk-content
description: Unregisters a Media Foundation transform (MFT).
old-location: mf\mftunregister.htm
old-project: medfound
ms.assetid: 2e63a098-5b83-4ea9-8149-4972f8ed0944
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 2e63a098-5b83-4ea9-8149-4972f8ed0944, MFTUnregister, MFTUnregister function [Media Foundation], mf.mftunregister, mfapi/MFTUnregister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFTUnregister
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFTUnregister function


## -description



          Unregisters a Media Foundation transform (MFT).
        


## -parameters




### -param clsidMFT [in]


            The CLSID of the MFT.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        This function removes the registry entries created by the <a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a> function.

It is safe to call <b>MFTUnregister</b> twice with the same CLSID. If the CLSID is not found in the registry, the function succeeds and does nothing.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

