---
UID: NF:mfidl.IMFSensorProfile.AddProfileFilter
title: IMFSensorProfile::AddProfileFilter
author: windows-sdk-content
description: Adds a profile filter to the specified media stream.
old-location: mf\imfsensorprofile_addprofilefilter.htm
old-project: medfound
ms.assetid: D79C83AA-A105-4320-80D8-F7A3753DF4C4
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: AddProfileFilter, AddProfileFilter method [Media Foundation], AddProfileFilter method [Media Foundation],IMFSensorProfile interface, IMFSensorProfile interface [Media Foundation],AddProfileFilter method, IMFSensorProfile.AddProfileFilter, IMFSensorProfile::AddProfileFilter, mf.imfsensorprofile_addprofilefilter, mfidl/IMFSensorProfile::AddProfileFilter
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfsensorgroup.dll
api_name:
 - IMFSensorProfile.AddProfileFilter
product: Windows
targetos: Windows
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorProfile::AddProfileFilter


## -description


Adds a profile filter to the specified media stream.


## -parameters




### -param StreamId [in]

The ID of the stream to add to.


### -param wzFilterSetString [in]

The filter to add.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt845815(v=VS.85).aspx">IMFSensorProfile</a>
 

 

