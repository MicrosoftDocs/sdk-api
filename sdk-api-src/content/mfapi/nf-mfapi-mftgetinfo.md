---
UID: NF:mfapi.MFTGetInfo
title: MFTGetInfo function
author: windows-sdk-content
description: Gets information from the registry about a Media Foundation transform (MFT).
old-location: mf\mftgetinfo.htm
tech.root: medfound
ms.assetid: d1bac1c7-3f9b-46b7-bdf7-c32983c648ee
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MFTGetInfo, MFTGetInfo function [Media Foundation], d1bac1c7-3f9b-46b7-bdf7-c32983c648ee, mf.mftgetinfo, mfapi/MFTGetInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MFTGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFTGetInfo function


## -description


Gets information from the registry about a Media Foundation transform (MFT).
        


## -parameters




### -param clsidMFT [in]

The CLSID of the MFT.
          


### -param pszName [out]

Receives a pointer to a wide-character string containing the friendly name of the MFT. The caller must free the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.
          


### -param ppInputTypes [out]

Receives a pointer to an array of <a href="https://msdn.microsoft.com/1d26b9ee-545a-4e47-9a68-b9e567f0dec4">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array describes an input format that the MFT supports. The caller must free the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.
          


### -param pcInputTypes [out]

Receives the number of elements in the <i>ppInputTypes</i> array. If <i>ppInputTypes</i> is <b>NULL</b>, this parameter is ignored and can be <b>NULL</b>.
          


### -param ppOutputTypes [out]

Receives a pointer to an array of <a href="https://msdn.microsoft.com/1d26b9ee-545a-4e47-9a68-b9e567f0dec4">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array describes an output format that the MFT supports. The caller must free the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.
          


### -param pcOutputTypes [out]

Receives the number of elements in the <i>ppOutputType</i> array. If <i>ppOutputTypes</i> is <b>NULL</b>, this parameter is ignored and can be <b>NULL</b>.
          


### -param ppAttributes [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store. The caller must release the interface. The attribute store might contain attributes that are stored in the registry for the specified MFT. (For more information, see <a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a>.)  If no attributes are stored in the registry for this MFT, the attribute store is empty. 

This parameter can be <b>NULL</b>.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a3bd2b3c-0b0b-4d64-99cc-6093c773f71c">MFTEnum</a>



<a href="https://msdn.microsoft.com/fb3a2b67-d3e4-4d5f-960a-3979f4780904">MFTRegister</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>



<a href="https://msdn.microsoft.com/76d2a703-4162-428e-a4ff-643e346eacfb">Registering and Enumerating MFTs</a>
 

 

