---
UID: NF:mfidl.IMFSensorProfileCollection.GetProfile
title: IMFSensorProfileCollection::GetProfile
author: windows-sdk-content
description: Retrieves the specified profile.
old-location: mf\imfsensorprofilecollection_getprofile.htm
tech.root: medfound
ms.assetid: 3E229A12-D53A-493F-9EFB-EA28131ABB10
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetProfile, GetProfile method [Media Foundation], GetProfile method [Media Foundation],IMFSensorProfileCollection interface, IMFSensorProfileCollection interface [Media Foundation],GetProfile method, IMFSensorProfileCollection.GetProfile, IMFSensorProfileCollection::GetProfile, mf.imfsensorprofilecollection_getprofile, mfidl/IMFSensorProfileCollection::GetProfile
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
 - IMFSensorProfileCollection.GetProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorProfileCollection::GetProfile


## -description


Retrieves the specified profile.


## -parameters




### -param Index [in]

Index of the profile to retrieve.


### -param ppProfile [out]

On success, returns a double pointer to an <a href="mf.imfsensorprofile">IMFSensorProfile</a> object that describes the specified sensor profile.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="mf.imfsensorprofilecollection">IMFSensorProfileCollection</a>
 

 

