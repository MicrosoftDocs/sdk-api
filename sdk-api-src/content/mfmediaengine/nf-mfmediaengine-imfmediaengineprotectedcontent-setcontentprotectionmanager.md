---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.SetContentProtectionManager
title: IMFMediaEngineProtectedContent::SetContentProtectionManager (mfmediaengine.h)
description: Sets the content protection manager (CPM).
helpviewer_keywords: ["IMFMediaEngineProtectedContent interface [Media Foundation]","SetContentProtectionManager method","IMFMediaEngineProtectedContent.SetContentProtectionManager","IMFMediaEngineProtectedContent::SetContentProtectionManager","SetContentProtectionManager","SetContentProtectionManager method [Media Foundation]","SetContentProtectionManager method [Media Foundation]","IMFMediaEngineProtectedContent interface","mf.imfmediaengineprotectedcontent_setcontentprotectionmanager","mfmediaengine/IMFMediaEngineProtectedContent::SetContentProtectionManager"]
old-location: mf\imfmediaengineprotectedcontent_setcontentprotectionmanager.htm
tech.root: mf
ms.assetid: 8F150CB5-43AB-4709-A254-636440113642
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineProtectedContent interface [Media Foundation],SetContentProtectionManager method, IMFMediaEngineProtectedContent.SetContentProtectionManager, IMFMediaEngineProtectedContent::SetContentProtectionManager, SetContentProtectionManager, SetContentProtectionManager method [Media Foundation], SetContentProtectionManager method [Media Foundation],IMFMediaEngineProtectedContent interface, mf.imfmediaengineprotectedcontent_setcontentprotectionmanager, mfmediaengine/IMFMediaEngineProtectedContent::SetContentProtectionManager
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineProtectedContent::SetContentProtectionManager
 - mfmediaengine/IMFMediaEngineProtectedContent::SetContentProtectionManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineProtectedContent.SetContentProtectionManager
---

# IMFMediaEngineProtectedContent::SetContentProtectionManager


## -description

Sets the content protection manager (CPM).

## -parameters

### -param pCPM [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager">IMFContentProtectionManager</a> interface, implemented by the caller.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Media Engine uses the CPM to handle events related to protected content, such as license acquisition.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent">IMFMediaEngineProtectedContent</a>