---
UID: NF:mbnapi.IMbnPin.GetPinManager
title: IMbnPin::GetPinManager (mbnapi.h)
description: Gets the IMbnPinManager.
helpviewer_keywords: ["GetPinManager","GetPinManager method [Microsoft Broadband Networks]","GetPinManager method [Microsoft Broadband Networks]","IMbnPin interface","IMbnPin interface [Microsoft Broadband Networks]","GetPinManager method","IMbnPin.GetPinManager","IMbnPin::GetPinManager","mbn.imbnpin_getpinmanager","mbnapi/IMbnPin::GetPinManager"]
old-location: mbn\imbnpin_getpinmanager.htm
tech.root: mbn
ms.assetid: 51957cb9-0204-4e07-aebf-1aaddb16b3c2
ms.date: 12/05/2018
ms.keywords: GetPinManager, GetPinManager method [Microsoft Broadband Networks], GetPinManager method [Microsoft Broadband Networks],IMbnPin interface, IMbnPin interface [Microsoft Broadband Networks],GetPinManager method, IMbnPin.GetPinManager, IMbnPin::GetPinManager, mbn.imbnpin_getpinmanager, mbnapi/IMbnPin::GetPinManager
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnPin::GetPinManager
 - mbnapi/IMbnPin::GetPinManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnPin.GetPinManager
---

# IMbnPin::GetPinManager


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a>.

## -parameters

### -param pinManager [out]

Pointer to the address of an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> to manage the PIN type.  When this function returns anything other than S_OK, this value is <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be used to retrieve an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> interface for the given PIN type.  The <b>GetPinManager</b> method retrieves an <b>IMbnPinManager</b> interface from the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> object passed in <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a> methods.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a>