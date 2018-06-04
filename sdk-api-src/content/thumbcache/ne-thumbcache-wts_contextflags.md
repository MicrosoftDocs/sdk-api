---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WTS_CONTEXTFLAGS enumeration


## -description


Specifies the context of a thumbnail extraction. Used by <a href="https://msdn.microsoft.com/AD333075-3358-4fee-BDEE-087B7012C93E">IThumbnailSettings::SetContext</a>.

Your thumbnail provider will set this flag based on the <a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_FLAGS</a> values that it received through the <a href="https://msdn.microsoft.com/5ea237fb-6b1c-4e87-a9f3-711ffa37b3dc">IThumbnailProvider::GetThumbnail</a> request.


## -enum-fields




### -field WTSCF_DEFAULT

None of the following options are set. Set in response to <a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_NONE</a>.


### -field WTSCF_APPSTYLE

Provide a thumbnail suitable to the Windows Store app UX guidelines. Set in response to <a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_APPSTYLE</a>.


### -field WTSCF_SQUARE

If necessary, crop the bitmap's dimensions so that is square. The length of the shortest side becomes the length of all sides. Set in response to <a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_CROPTOSQUARE</a>.


### -field WTSCF_WIDE

Stretch and crop the bitmap so that its height is 0.7 times its width. Set in response to <a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_WIDETHUMBNAILS</a>.


### -field WTSCF_FAST

If not cached, only extract the thumbnail if it is embedded in EXIF format, typically 96x96. Set in response to <a href="https://msdn.microsoft.com/D9C84E86-35AF-437f-966E-BABD02B824C0">WTS_FASTEXTRACT</a>.

