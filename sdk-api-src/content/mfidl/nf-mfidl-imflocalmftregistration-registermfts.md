---
UID: NF:mfidl.IMFLocalMFTRegistration.RegisterMFTs
title: IMFLocalMFTRegistration::RegisterMFTs
author: windows-sdk-content
description: Registers one or more Media Foundation transforms (MFTs) in the caller's process.
old-location: mf\imflocalmftregistration_registermfts.htm
old-project: medfound
ms.assetid: 3f77b5b9-94af-42b1-83ca-cb3310083632
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFLocalMFTRegistration interface [Media Foundation],RegisterMFTs method, IMFLocalMFTRegistration.RegisterMFTs, IMFLocalMFTRegistration::RegisterMFTs, RegisterMFTs, RegisterMFTs method [Media Foundation], RegisterMFTs method [Media Foundation],IMFLocalMFTRegistration interface, mf.imflocalmftregistration_registermfts, mfidl/IMFLocalMFTRegistration::RegisterMFTs
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFLocalMFTRegistration.RegisterMFTs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFLocalMFTRegistration::RegisterMFTs


## -description


Registers one or more Media Foundation transforms (MFTs) in the caller's process.


## -parameters




### -param pMFTs [in]

A pointer to an array of <a href="https://msdn.microsoft.com/7d610edf-89e3-4ff3-9ad8-b92ee50df522">MFT_REGISTRATION_INFO</a> structures.


### -param cMFTs [in]

The number of elements in the <i>pMFTs</i> array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is similar to the <a href="https://msdn.microsoft.com/80c45ac3-4487-41bf-a5f5-f459db3cd700">MFTRegisterLocalByCLSID</a> function. It registers one or more MFTs in the caller's process. These MFTs can be enumerated by calling the <a href="https://msdn.microsoft.com/e065ae51-85dd-48ef-9322-de4ade62c0fe">MFTEnumEx</a> function with the <b>MFT_ENUM_FLAG_LOCALMFT</b> flag.

Unlike <a href="https://msdn.microsoft.com/80c45ac3-4487-41bf-a5f5-f459db3cd700">MFTRegisterLocalByCLSID</a>, however, this method also makes the MFT available in the Protected Media Path (PMP) process, and is therefore useful if you are using the Media Session inside the PMP. For more information, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/cb492e68-3d8a-49b2-8c0b-bee8065b53a8">MFCreatePMPMediaSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e540a93a-ecce-4c5b-a121-b0f868a2af41">IMFLocalMFTRegistration</a>
 

 

