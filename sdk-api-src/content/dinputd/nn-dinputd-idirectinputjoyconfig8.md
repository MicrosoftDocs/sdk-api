---
UID: NN:dinputd.IDirectInputJoyConfig8
title: IDirectInputJoyConfig8 (dinputd.h)
description: IDirectInputJoyConfig8 interface contains methods that allow hardware developers who are writing property sheets to write and read information to and from the registry.
helpviewer_keywords: ["IDirectInputJoyConfig8","IDirectInputJoyConfig8 interface [Human Input Devices]","IDirectInputJoyConfig8 interface [Human Input Devices]","described","di_ref_75413607-c6c1-4341-892a-7f313a0ed9d5.xml","dinputd/IDirectInputJoyConfig8","hid.idirectinputjoyconfig8"]
old-location: hid\idirectinputjoyconfig8.htm
tech.root: hid
ms.assetid: baae99bf-a826-45d0-bab2-76a5736bd378
ms.date: 12/05/2018
ms.keywords: IDirectInputJoyConfig8, IDirectInputJoyConfig8 interface [Human Input Devices], IDirectInputJoyConfig8 interface [Human Input Devices],described, di_ref_75413607-c6c1-4341-892a-7f313a0ed9d5.xml, dinputd/IDirectInputJoyConfig8, hid.idirectinputjoyconfig8
req.header: dinputd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectInputJoyConfig8
 - dinputd/IDirectInputJoyConfig8
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dinputd.h
api_name:
 - IDirectInputJoyConfig8
---

# IDirectInputJoyConfig8 interface


## -description

<b>IDirectInputJoyConfig8</b> interface contains methods that allow hardware developers who are writing property sheets 
 to write and read information to and from the registry. If you need to open registry keys, you should use the 
 <a href="/previous-versions/windows/hardware/drivers/ff540995(v=vs.85)">IDirectInputJoyConfig8::OpenConfigKey</a> and 
 <a href="/windows/desktop/api/dinputd/nf-dinputd-idirectinputjoyconfig8-opentypekey">IDirectInputJoyConfig8::OpenTypeKey</a> methods rather 
 than opening registry keys directly. Using either of these methods ensures that the correct registry branch is opened. 
 In addition, the <b>IDirectInputJoyConfig8</b> interface will be supported in future versions of DirectInput when the underlying registry data 
 may be structured differently.

## -inheritance

The <b>IDirectInputJoyConfig8</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectInputJoyConfig8</b> also has these types of members:

