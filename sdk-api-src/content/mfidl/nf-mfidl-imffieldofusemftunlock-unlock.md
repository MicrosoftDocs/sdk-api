---
UID: NF:mfidl.IMFFieldOfUseMFTUnlock.Unlock
title: IMFFieldOfUseMFTUnlock::Unlock (mfidl.h)
author: windows-sdk-content
description: Unlocks a Media Foundation transform (MFT) so that the application can use it.
old-location: mf\imffieldofusemftunlock_unlock.htm
tech.root: medfound
ms.assetid: 54b15e72-6551-4162-90ca-a9bed68ca62f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFFieldOfUseMFTUnlock interface [Media Foundation],Unlock method, IMFFieldOfUseMFTUnlock.Unlock, IMFFieldOfUseMFTUnlock::Unlock, Unlock, Unlock method [Media Foundation], Unlock method [Media Foundation],IMFFieldOfUseMFTUnlock interface, mf.imffieldofusemftunlock_unlock, mfidl/IMFFieldOfUseMFTUnlock::Unlock
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
 - IMFFieldOfUseMFTUnlock.Unlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFFieldOfUseMFTUnlock::Unlock


## -description


Unlocks a Media Foundation transform (MFT) so that the application can use it.


## -parameters




### -param pUnkMFT [in]

A pointer to the <b>IUnknown</b> interface of the MFT.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method authenticates the caller, using a private communication channel between the MFT and the object that implements the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock">IMFFieldOfUseMFTUnlock</a> interface. The details of the communication depend entirely on the implementation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/field-of-use-restrictions">Field of Use Restrictions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock">IMFFieldOfUseMFTUnlock</a>
 

 

