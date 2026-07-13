---
UID: NN:mbnapi.IMbnConnectionProfile
title: IMbnConnectionProfile (mbnapi.h)
description: This interface accesses connection parameters and preferences stored in Mobile Broadband profiles.
helpviewer_keywords: ["IMbnConnectionProfile","IMbnConnectionProfile interface [Microsoft Broadband Networks]","IMbnConnectionProfile interface [Microsoft Broadband Networks]","described","mbn.imbnconnectionprofile","mbnapi/IMbnConnectionProfile"]
old-location: mbn\imbnconnectionprofile.htm
tech.root: mbn
ms.assetid: f7730efe-e367-4642-8482-2a23052bab0c
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfile, IMbnConnectionProfile interface [Microsoft Broadband Networks], IMbnConnectionProfile interface [Microsoft Broadband Networks],described, mbn.imbnconnectionprofile, mbnapi/IMbnConnectionProfile
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnConnectionProfile
 - mbnapi/IMbnConnectionProfile
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
 - IMbnConnectionProfile
---

# IMbnConnectionProfile interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This interface accesses connection parameters and preferences stored in Mobile Broadband profiles.

## -inheritance

The <b>IMbnConnectionProfile</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionProfile</b> also has these types of members:

## -remarks

<b>IMbnConnectionProfile</b> objects are provided by calls to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-getconnectionprofile">GetConnectionProfile</a> and <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-getconnectionprofiles">GetConnectionProfiles</a> methods of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a> interface.
