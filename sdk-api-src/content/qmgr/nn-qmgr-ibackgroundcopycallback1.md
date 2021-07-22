---
UID: NN:qmgr.IBackgroundCopyCallback1
title: IBackgroundCopyCallback1 (qmgr.h)
description: Implement the IBackgroundCopyCallback1 interface to receive notification when events occur.
helpviewer_keywords: ["IBackgroundCopyCallback1","IBackgroundCopyCallback1 interface [BITS]","IBackgroundCopyCallback1 interface [BITS]","described","bits.ibackgroundcopycallback1","qmgr/IBackgroundCopyCallback1"]
old-location: bits\ibackgroundcopycallback1.htm
tech.root: Bits
ms.assetid: d5d22cf6-d9b5-4001-a0ac-f67d59dde779
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyCallback1, IBackgroundCopyCallback1 interface [BITS], IBackgroundCopyCallback1 interface [BITS],described, bits.ibackgroundcopycallback1, qmgr/IBackgroundCopyCallback1
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyCallback1
 - qmgr/IBackgroundCopyCallback1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qmgr.h
api_name:
 - IBackgroundCopyCallback1
 - IBackgroundCopyCallback1.OnProgress
 - IBackgroundCopyCallback1.OnProgressEx
---

# IBackgroundCopyCallback1 interface


## -description

<p class="CCE_Message">[<b>IBackgroundCopyCallback1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions.  Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Implement the <b>IBackgroundCopyCallback1</b> interface to receive notification when events occur. Applications use this interface as an option to polling for the state of the group.

To receive notifications, call the <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopygroup-setprop">IBackgroundCopyGroup::SetProp</a> method to set the <b>GROUPPROP_NOTIFYCLSID</b> and <b>GROUPPROP_NOTIFYFLAGS</b> properties. 

QMGR uses the interface pointer while it is valid (the interface pointer becomes invalid when your application exits). When your application restarts, you must reset the <b>GROUPPROP_NOTIFYCLSID</b> property on those groups that QMGR is still processing. 
<div class="alert"><b>Note</b>  QMGR activates the new object inside the scope of the client process; notifications are not run in their own process.  QMGR creates a new object of that CLSID and passes an interface pointer to BITS. </div><div> </div>You must implement all methods of the <b>IBackgroundCopyCallback1</b> interface. At a minimum, the method must return <b>S_OK</b>. To reduce the chance that your callback blocks BITS, keep your implementation short. 

If an administrator takes ownership of the group, the notification callbacks are made in the context of the user who requested notification.

## -inheritance

The <b>IBackgroundCopyCallback1</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyCallback1</b> also has these types of members:

