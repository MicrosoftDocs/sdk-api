---
UID: NF:mfidl.IMFPMPHostApp.ActivateClassById
title: IMFPMPHostApp::ActivateClassById (mfidl.h)
description: Creates a Windows Runtime object in the protected media path (PMP) process.
helpviewer_keywords: ["ActivateClassById","ActivateClassById method [Media Foundation]","ActivateClassById method [Media Foundation]","IMFPMPHostApp interface","IMFPMPHostApp interface [Media Foundation]","ActivateClassById method","IMFPMPHostApp.ActivateClassById","IMFPMPHostApp::ActivateClassById","mf.imfpmphostapp_activateclassbyid","mfidl/IMFPMPHostApp::ActivateClassById"]
old-location: mf\imfpmphostapp_activateclassbyid.htm
tech.root: mf
ms.assetid: e0e14171-fcc9-418a-a93d-3cdbae254a3f
ms.date: 12/05/2018
ms.keywords: ActivateClassById, ActivateClassById method [Media Foundation], ActivateClassById method [Media Foundation],IMFPMPHostApp interface, IMFPMPHostApp interface [Media Foundation],ActivateClassById method, IMFPMPHostApp.ActivateClassById, IMFPMPHostApp::ActivateClassById, mf.imfpmphostapp_activateclassbyid, mfidl/IMFPMPHostApp::ActivateClassById
req.header: mfidl.h
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
 - IMFPMPHostApp::ActivateClassById
 - mfidl/IMFPMPHostApp::ActivateClassById
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFPMPHostApp.ActivateClassById
---

# IMFPMPHostApp::ActivateClassById


## -description

Creates a Windows Runtime object in the protected media path (PMP) process.

## -parameters

### -param id [in]

Id of object to create.

### -param pStream [in]

Data to be passed to the object by way of a <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>.

### -param riid [in]

The interface identifier (IID) of the interface to retrieve.

### -param ppv [out]

Receives a pointer to the created object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp">IMFPMPHostApp</a>