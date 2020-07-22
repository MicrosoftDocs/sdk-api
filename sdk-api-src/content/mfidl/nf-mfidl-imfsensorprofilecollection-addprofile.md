---
UID: NF:mfidl.IMFSensorProfileCollection.AddProfile
title: IMFSensorProfileCollection::AddProfile (mfidl.h)
description: Adds the specified profile to the collection.
helpviewer_keywords: ["AddProfile","AddProfile method [Media Foundation]","AddProfile method [Media Foundation]","IMFSensorProfileCollection interface","IMFSensorProfileCollection interface [Media Foundation]","AddProfile method","IMFSensorProfileCollection.AddProfile","IMFSensorProfileCollection::AddProfile","mf.imfsensorprofilecollection_addprofile","mfidl/IMFSensorProfileCollection::AddProfile"]
old-location: mf\imfsensorprofilecollection_addprofile.htm
tech.root: mf
ms.assetid: 4997E69B-6444-4603-ABCF-4E2526B5AC23
ms.date: 12/05/2018
ms.keywords: AddProfile, AddProfile method [Media Foundation], AddProfile method [Media Foundation],IMFSensorProfileCollection interface, IMFSensorProfileCollection interface [Media Foundation],AddProfile method, IMFSensorProfileCollection.AddProfile, IMFSensorProfileCollection::AddProfile, mf.imfsensorprofilecollection_addprofile, mfidl/IMFSensorProfileCollection::AddProfile
f1_keywords:
- mfidl/IMFSensorProfileCollection.AddProfile
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mfsensorgroup.dll
api_name:
- IMFSensorProfileCollection.AddProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorProfileCollection::AddProfile


## -description


Adds the specified profile to the collection.


## -parameters




### -param pProfile [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile">IMFSensorProfile</a> object describing the profile to add.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection">IMFSensorProfileCollection</a>
 

 

