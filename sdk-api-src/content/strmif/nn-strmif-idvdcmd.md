---
UID: NN:strmif.IDvdCmd
title: IDvdCmd (strmif.h)
description: The IDvdCmd interface waits for DVD commands to start or end.The DVD Navigator creates synchronization objects that expose this interface.
helpviewer_keywords: ["IDvdCmd","IDvdCmd interface [DirectShow]","IDvdCmd interface [DirectShow]","described","IDvdCmdInterface","dshow.idvdcmd","strmif/IDvdCmd"]
old-location: dshow\idvdcmd.htm
tech.root: dshow
ms.assetid: 85f9b208-ddc2-4d9c-a30b-b666c81a49d2
ms.date: 12/05/2018
ms.keywords: IDvdCmd, IDvdCmd interface [DirectShow], IDvdCmd interface [DirectShow],described, IDvdCmdInterface, dshow.idvdcmd, strmif/IDvdCmd
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdCmd
 - strmif/IDvdCmd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdCmd
---

# IDvdCmd interface


## -description

The <code>IDvdCmd</code> interface waits for DVD commands to start or end.

The DVD Navigator creates synchronization objects that expose this interface. The application can use the object to block the DVD Navigator until the command starts or completes. For more information on using this interface, see <a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>. (This topic also discusses other ways to synchronize commands without using synchronization objects.)

## -inheritance

The <b>IDvdCmd</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdCmd</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>
