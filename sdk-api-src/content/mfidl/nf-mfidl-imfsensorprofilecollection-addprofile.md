---
UID: NF:mfidl.IMFSensorProfileCollection.AddProfile
title: IMFSensorProfileCollection::AddProfile
author: windows-driver-content
description: Adds the specified profile to the collection.
old-location: mf\imfsensorprofilecollection_addprofile.htm
old-project: medfound
ms.assetid: 4997E69B-6444-4603-ABCF-4E2526B5AC23
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: AddProfile, AddProfile method [Media Foundation], AddProfile method [Media Foundation],IMFSensorProfileCollection interface, IMFSensorProfileCollection interface [Media Foundation],AddProfile method, IMFSensorProfileCollection.AddProfile, IMFSensorProfileCollection::AddProfile, mf.imfsensorprofilecollection_addprofile, mfidl/IMFSensorProfileCollection::AddProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mfsensorgroup.dll
api_name:
-	IMFSensorProfileCollection.AddProfile
product: Windows
targetos: Windows
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorProfileCollection::AddProfile


## -description


Adds the specified profile to the collection.


## -parameters




### -param pProfile [in]

Pointer to an <a href="https://msdn.microsoft.com/58D9FE3F-0F42-4262-B1BE-336BFA2E4BC7">IMFSensorProfile</a> object describing the profile to add.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/406EDC3F-39AD-41E0-A8AA-E4476C93F353">IMFSensorProfileCollection</a>
 

 

