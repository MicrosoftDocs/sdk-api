---
UID: NF:mfapi.MFGetMFTMerit
title: MFGetMFTMerit function
author: windows-driver-content
description: Gets the merit value of a hardware codec.
old-location: mf\mfgetmftmerit.htm
old-project: medfound
ms.assetid: 69029cf3-7f34-4bb1-8dfd-fa9a8d1a63c9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MFGetMFTMerit, MFGetMFTMerit function [Media Foundation], mf.mfgetmftmerit, mfapi/MFGetMFTMerit
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFGetMFTMerit
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFGetMFTMerit function


## -description


Gets the merit value of a hardware codec.


## -parameters




### -param pMFT [in, out]

A pointer to the <b>IUnknown</b> interface of the Media Foundation transform (MFT) that represents the codec.


### -param cbVerifier [in]

The size, in bytes, of the <i>verifier</i> array.


### -param verifier [in]

The address of a buffer that contains one of the following:

<ul>
<li>The class identifier (CLSID) of the MFT.</li>
<li>A null-terminated wide-character string that contains the symbol link for the underlying hardware device. Include the size of the terminating null in the value of <i>cbVerifier</i>.</li>
</ul>

### -param merit [out]

Receives the merit value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The function fails if the MFT does not represent a hardware device with a valid Output Protection Manager (OPM) certificate.
      




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/51987a79-78bf-41b2-8349-8c2725dd89d6">OPM_GET_CODEC_INFO</a>
 

 

