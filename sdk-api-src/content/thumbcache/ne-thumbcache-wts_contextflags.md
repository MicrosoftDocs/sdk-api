---
UID: NE:thumbcache.WTS_CONTEXTFLAGS
title: WTS_CONTEXTFLAGS
author: windows-sdk-content
description: Specifies the context of a thumbnail extraction. Used by IThumbnailSettings::SetContext.
old-location: shell\WTS_CONTEXTFLAGS.htm
old-project: shell
ms.assetid: 062B148E-19FB-4bcd-82CE-669B2ACD0BF6
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: WTSCF_APPSTYLE, WTSCF_DEFAULT, WTSCF_FAST, WTSCF_SQUARE, WTSCF_WIDE, WTS_CONTEXTFLAGS, WTS_CONTEXTFLAGS enumeration [Windows Shell], shell.WTS_CONTEXTFLAGS, thumbcache/WTSCF_APPSTYLE, thumbcache/WTSCF_DEFAULT, thumbcache/WTSCF_FAST, thumbcache/WTSCF_SQUARE, thumbcache/WTSCF_WIDE, thumbcache/WTS_CONTEXTFLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_CONTEXTFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Thumbcache.h
api_name:
 - WTS_CONTEXTFLAGS
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
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

