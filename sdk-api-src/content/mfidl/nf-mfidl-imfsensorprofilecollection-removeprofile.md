---
UID: NF:mfidl.IMFSensorProfileCollection.RemoveProfile
title: IMFSensorProfileCollection::RemoveProfile
author: windows-sdk-content
description: Removes the specified profile based on the specified profile ID.
old-location: mf\imfsensorprofilecollection_removeprofile.htm
tech.root: medfound
ms.assetid: E0A0C773-7B60-46C7-9B89-07DF5CAA1E84
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFSensorProfileCollection interface [Media Foundation],RemoveProfile method, IMFSensorProfileCollection.RemoveProfile, IMFSensorProfileCollection::RemoveProfile, RemoveProfile, RemoveProfile method [Media Foundation], RemoveProfile method [Media Foundation],IMFSensorProfileCollection interface, mf.imfsensorprofilecollection_removeprofile, mfidl/IMFSensorProfileCollection::RemoveProfile
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
 - IMFSensorProfileCollection.RemoveProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorProfileCollection::RemoveProfile


## -description


removes the specified profile based on the specified profile ID.


## -parameters




### -param ProfileId [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Mt845826(v=VS.85).aspx">SENSORPROFILEID</a> of the profile to remove.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt845816(v=VS.85).aspx">IMFSensorProfileCollection</a>
 

 

