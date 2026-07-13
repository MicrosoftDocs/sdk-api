---
UID: NE:thumbcache.WTS_CONTEXTFLAGS
title: WTS_CONTEXTFLAGS (thumbcache.h)
description: Specifies the context of a thumbnail extraction. Used by IThumbnailSettings::SetContext.
helpviewer_keywords: ["WTSCF_APPSTYLE","WTSCF_DEFAULT","WTSCF_FAST","WTSCF_SQUARE","WTSCF_WIDE","WTS_CONTEXTFLAGS","WTS_CONTEXTFLAGS enumeration [Windows Shell]","shell.WTS_CONTEXTFLAGS","thumbcache/WTSCF_APPSTYLE","thumbcache/WTSCF_DEFAULT","thumbcache/WTSCF_FAST","thumbcache/WTSCF_SQUARE","thumbcache/WTSCF_WIDE","thumbcache/WTS_CONTEXTFLAGS"]
old-location: shell\WTS_CONTEXTFLAGS.htm
tech.root: shell
ms.assetid: 062B148E-19FB-4bcd-82CE-669B2ACD0BF6
ms.date: 12/05/2018
ms.keywords: WTSCF_APPSTYLE, WTSCF_DEFAULT, WTSCF_FAST, WTSCF_SQUARE, WTSCF_WIDE, WTS_CONTEXTFLAGS, WTS_CONTEXTFLAGS enumeration [Windows Shell], shell.WTS_CONTEXTFLAGS, thumbcache/WTSCF_APPSTYLE, thumbcache/WTSCF_DEFAULT, thumbcache/WTSCF_FAST, thumbcache/WTSCF_SQUARE, thumbcache/WTSCF_WIDE, thumbcache/WTS_CONTEXTFLAGS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTS_CONTEXTFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTS_CONTEXTFLAGS
 - thumbcache/WTS_CONTEXTFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Thumbcache.h
api_name:
 - WTS_CONTEXTFLAGS
---

# WTS_CONTEXTFLAGS enumeration


## -description

Specifies the context of a thumbnail extraction. Used by <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailsettings-setcontext">IThumbnailSettings::SetContext</a>.

Your thumbnail provider will set this flag based on the <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_FLAGS</a> values that it received through the <a href="/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail">IThumbnailProvider::GetThumbnail</a> request.

## -enum-fields

### -field WTSCF_DEFAULT:0

None of the following options are set. Set in response to <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_NONE</a>.

### -field WTSCF_APPSTYLE:0x1

Provide a thumbnail suitable to the Windows Store app UX guidelines. Set in response to <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_APPSTYLE</a>.

### -field WTSCF_SQUARE:0x2

If necessary, crop the bitmap's dimensions so that is square. The length of the shortest side becomes the length of all sides. Set in response to <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_CROPTOSQUARE</a>.

### -field WTSCF_WIDE:0x4

Stretch and crop the bitmap so that its height is 0.7 times its width. Set in response to <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_WIDETHUMBNAILS</a>.

### -field WTSCF_FAST:0x8

If not cached, only extract the thumbnail if it is embedded in EXIF format, typically 96x96. Set in response to <a href="/windows/desktop/api/thumbcache/ne-thumbcache-wts_flags">WTS_FASTEXTRACT</a>.
