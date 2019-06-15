---
UID: NF:mfidl.IMFLocalMFTRegistration.RegisterMFTs
title: IMFLocalMFTRegistration::RegisterMFTs (mfidl.h)
author: windows-sdk-content
description: Registers one or more Media Foundation transforms (MFTs) in the caller's process.
old-location: mf\imflocalmftregistration_registermfts.htm
tech.root: medfound
ms.assetid: 3f77b5b9-94af-42b1-83ca-cb3310083632
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFLocalMFTRegistration interface [Media Foundation],RegisterMFTs method, IMFLocalMFTRegistration.RegisterMFTs, IMFLocalMFTRegistration::RegisterMFTs, RegisterMFTs, RegisterMFTs method [Media Foundation], RegisterMFTs method [Media Foundation],IMFLocalMFTRegistration interface, mf.imflocalmftregistration_registermfts, mfidl/IMFLocalMFTRegistration::RegisterMFTs
ms.topic: method
req.header: mfidl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFLocalMFTRegistration.RegisterMFTs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFLocalMFTRegistration::RegisterMFTs


## -description


Registers one or more Media Foundation transforms (MFTs) in the caller's process.


## -parameters




### -param pMFTs [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ns-mfidl-_mft_registration_info">MFT_REGISTRATION_INFO</a> structures.


### -param cMFTs [in]

The number of elements in the <i>pMFTs</i> array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is similar to the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid">MFTRegisterLocalByCLSID</a> function. It registers one or more MFTs in the caller's process. These MFTs can be enumerated by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> function with the <b>MFT_ENUM_FLAG_LOCALMFT</b> flag.

Unlike <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid">MFTRegisterLocalByCLSID</a>, however, this method also makes the MFT available in the Protected Media Path (PMP) process, and is therefore useful if you are using the Media Session inside the PMP. For more information, see the following topics:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imflocalmftregistration">IMFLocalMFTRegistration</a>
 

 

