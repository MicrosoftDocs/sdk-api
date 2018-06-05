---
UID: NF:mfidl.IMFSensorProfileCollection.GetProfile
title: IMFSensorProfileCollection::GetProfile
author: windows-sdk-content
description: Retrieves the specified profile.
old-location: mf\imfsensorprofilecollection_getprofile.htm
old-project: medfound
ms.assetid: 3E229A12-D53A-493F-9EFB-EA28131ABB10
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetProfile, GetProfile method [Media Foundation], GetProfile method [Media Foundation],IMFSensorProfileCollection interface, IMFSensorProfileCollection interface [Media Foundation],GetProfile method, IMFSensorProfileCollection.GetProfile, IMFSensorProfileCollection::GetProfile, mf.imfsensorprofilecollection_getprofile, mfidl/IMFSensorProfileCollection::GetProfile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mfsensorgroup.dll
api_name:
-	IMFSensorProfileCollection.GetProfile
product: Windows
targetos: Windows
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorProfileCollection::GetProfile


## -description


Retrieves the specified profile.


## -parameters




### -param Index [in]

Index of the profile to retrieve.


### -param ppProfile [out]

On success, returns a double pointer to an <a href="https://msdn.microsoft.com/58D9FE3F-0F42-4262-B1BE-336BFA2E4BC7">IMFSensorProfile</a> object that describes the specified sensor profile.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/406EDC3F-39AD-41E0-A8AA-E4476C93F353">IMFSensorProfileCollection</a>
 

 

