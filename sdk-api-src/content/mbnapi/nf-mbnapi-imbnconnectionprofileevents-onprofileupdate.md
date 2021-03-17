---
UID: NF:mbnapi.IMbnConnectionProfileEvents.OnProfileUpdate
title: IMbnConnectionProfileEvents::OnProfileUpdate (mbnapi.h)
description: A notification method that indicates that profile update operation has completed.
helpviewer_keywords: ["IMbnConnectionProfileEvents interface [Microsoft Broadband Networks]","OnProfileUpdate method","IMbnConnectionProfileEvents.OnProfileUpdate","IMbnConnectionProfileEvents::OnProfileUpdate","OnProfileUpdate","OnProfileUpdate method [Microsoft Broadband Networks]","OnProfileUpdate method [Microsoft Broadband Networks]","IMbnConnectionProfileEvents interface","mbn.imbnconnectionprofileevents_onprofileupdatecomplete","mbnapi/IMbnConnectionProfileEvents::OnProfileUpdate"]
old-location: mbn\imbnconnectionprofileevents_onprofileupdatecomplete.htm
tech.root: mbn
ms.assetid: eb113544-0c89-4b38-a2f4-c67c639fe8a3
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfileEvents interface [Microsoft Broadband Networks],OnProfileUpdate method, IMbnConnectionProfileEvents.OnProfileUpdate, IMbnConnectionProfileEvents::OnProfileUpdate, OnProfileUpdate, OnProfileUpdate method [Microsoft Broadband Networks], OnProfileUpdate method [Microsoft Broadband Networks],IMbnConnectionProfileEvents interface, mbn.imbnconnectionprofileevents_onprofileupdatecomplete, mbnapi/IMbnConnectionProfileEvents::OnProfileUpdate
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
 - IMbnConnectionProfileEvents::OnProfileUpdate
 - mbnapi/IMbnConnectionProfileEvents::OnProfileUpdate
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
 - IMbnConnectionProfileEvents.OnProfileUpdate
---

# IMbnConnectionProfileEvents::OnProfileUpdate


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

A notification method that indicates that profile update operation has completed.

## -parameters

### -param newProfile [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> interface that represents the profile that has changed.

## -returns

This method must return <b>S_OK</b>.

## -remarks

<b>OnProfileUpdate</b> is called to notify a registered application of the completion of an operation initiated by a call to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofile-updateprofile">UpdateProfile</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a> interface, or the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile">CreateConnectionProfile</a> of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofileevents">IMbnConnectionProfileEvents</a>