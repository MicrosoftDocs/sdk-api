---
UID: NF:wmcontainer.IMFASFProfile.Clone
title: IMFASFProfile::Clone (wmcontainer.h)
description: Creates a copy of the Advanced Systems Format profile object.
helpviewer_keywords: ["Clone","Clone method [Media Foundation]","Clone method [Media Foundation]","IMFASFProfile interface","IMFASFProfile interface [Media Foundation]","Clone method","IMFASFProfile.Clone","IMFASFProfile::Clone","e91d3d2c-ef08-460e-b6f8-e8eed8df5a67","mf.imfasfprofile_clone","wmcontainer/IMFASFProfile::Clone"]
old-location: mf\imfasfprofile_clone.htm
tech.root: mf
ms.assetid: e91d3d2c-ef08-460e-b6f8-e8eed8df5a67
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Media Foundation], Clone method [Media Foundation],IMFASFProfile interface, IMFASFProfile interface [Media Foundation],Clone method, IMFASFProfile.Clone, IMFASFProfile::Clone, e91d3d2c-ef08-460e-b6f8-e8eed8df5a67, mf.imfasfprofile_clone, wmcontainer/IMFASFProfile::Clone
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFProfile::Clone
 - wmcontainer/IMFASFProfile::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFProfile.Clone
---

# IMFASFProfile::Clone


## -description

Creates a copy of the Advanced Systems Format profile object.

## -parameters

### -param ppIProfile [out]

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a> interface of the new object. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The cloned object is completely independent of the original.

## -see-also

<a href="/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile">IMFASFProfile</a>