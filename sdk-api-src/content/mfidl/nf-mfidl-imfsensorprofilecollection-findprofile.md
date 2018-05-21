---
UID: NF:mfidl.IMFSensorProfileCollection.FindProfile
title: IMFSensorProfileCollection::FindProfile
author: windows-driver-content
description: Finds a profile based on the specified profile ID.
old-location: mf\imfsensorprofilecollection_findprofile.htm
old-project: medfound
ms.assetid: 3EC77F69-717F-404F-9C8C-F420F360CB83
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: FindProfile, FindProfile method [Media Foundation], FindProfile method [Media Foundation],IMFSensorProfileCollection interface, IMFSensorProfileCollection interface [Media Foundation],FindProfile method, IMFSensorProfileCollection.FindProfile, IMFSensorProfileCollection::FindProfile, mf.imfsensorprofilecollection_findprofile, mfidl/IMFSensorProfileCollection::FindProfile
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
-	Mfsensorgroup.lib
-	Mfsensorgroup.dll
api_name:
-	IMFSensorProfileCollection.FindProfile
product: Windows
targetos: Windows
req.lib: Mfsensorgroup.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorProfileCollection::FindProfile


## -description


Finds a profile based on the specified profile ID.


## -parameters




### -param ProfileId [in]

Pointer to the The ID of the profile to find.


### -param ppProfile [out]

On success, returns a double pointer to the profile.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/406EDC3F-39AD-41E0-A8AA-E4476C93F353">IMFSensorProfileCollection</a>
 

 

