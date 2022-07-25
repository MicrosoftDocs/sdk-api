---
UID: NN:bits.IBackgroundCopyManager
title: IBackgroundCopyManager (bits.h)
description: Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.
helpviewer_keywords: ["IBackgroundCopyManager","IBackgroundCopyManager interface [BITS]","IBackgroundCopyManager interface [BITS]","described","_drz_ibackgroundcopymanager","bits.ibackgroundcopymanager","bits/IBackgroundCopyManager"]
old-location: bits\ibackgroundcopymanager.htm
tech.root: Bits
ms.assetid: fc98dfb3-7e10-421d-b722-223bd8a65330
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyManager, IBackgroundCopyManager interface [BITS], IBackgroundCopyManager interface [BITS],described, _drz_ibackgroundcopymanager, bits.ibackgroundcopymanager, bits/IBackgroundCopyManager
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyManager
 - bits/IBackgroundCopyManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyManager
---

# IBackgroundCopyManager interface


## -description

Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.

For information on how to create an instance of this interface, see 
<a href="/windows/desktop/Bits/connecting-to-the-bits-service">Connecting to the BITS Service</a>.

## -inheritance

The <b>IBackgroundCopyManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyManager</b> also has these types of members:

## -remarks

<b>Windows Vista and later:  </b>When an ActiveX control tries to instantiate this interface from an Internet Explorer process, the call will fail with access denied. This is because COM does not allow lower-integrity clients to bind to class instances at higher integrity levels. For details, see <a href="/previous-versions/windows/internet-explorer/ie-developer/">Understanding and Working in Protected Mode Internet Explorer</a> and <a href="/previous-versions/dotnet/articles/bb625962(v=msdn.10)">How the Integrity Mechanism Is Implemented in Windows Vista</a>. A user can workaround the issue by adding the website to the Trusted site zone.

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="/windows/desktop/api/bits/nn-bits-ienumbackgroundcopyjobs">IEnumBackgroundCopyJobs</a>
