---
UID: NF:mfidl.IMFSensorProfileCollection.FindProfile
title: IMFSensorProfileCollection::FindProfile (mfidl.h)
author: windows-sdk-content
description: Finds a profile based on the specified profile ID.
old-location: mf\imfsensorprofilecollection_findprofile.htm
tech.root: medfound
ms.assetid: 3EC77F69-717F-404F-9C8C-F420F360CB83
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindProfile, FindProfile method [Media Foundation], FindProfile method [Media Foundation],IMFSensorProfileCollection interface, IMFSensorProfileCollection interface [Media Foundation],FindProfile method, IMFSensorProfileCollection.FindProfile, IMFSensorProfileCollection::FindProfile, mf.imfsensorprofilecollection_findprofile, mfidl/IMFSensorProfileCollection::FindProfile
ms.topic: method
f1_keywords: 
 - "mfidl/IMFSensorProfileCollection.FindProfile"
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfsensorgroup.lib
 - Mfsensorgroup.dll
api_name:
 - IMFSensorProfileCollection.FindProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection">IMFSensorProfileCollection</a>
 

 

