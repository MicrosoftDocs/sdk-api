---
UID: NF:mfidl.IMFStreamDescriptor.GetStreamIdentifier
title: IMFStreamDescriptor::GetStreamIdentifier (mfidl.h)
description: Retrieves an identifier for the stream.
helpviewer_keywords: ["GetStreamIdentifier","GetStreamIdentifier method [Media Foundation]","GetStreamIdentifier method [Media Foundation]","IMFStreamDescriptor interface","IMFStreamDescriptor interface [Media Foundation]","GetStreamIdentifier method","IMFStreamDescriptor.GetStreamIdentifier","IMFStreamDescriptor::GetStreamIdentifier","d282ee48-6145-4557-8fa7-786b893327fa","mf.imfstreamdescriptor_getstreamidentifier","mfidl/IMFStreamDescriptor::GetStreamIdentifier"]
old-location: mf\imfstreamdescriptor_getstreamidentifier.htm
tech.root: mf
ms.assetid: d282ee48-6145-4557-8fa7-786b893327fa
ms.date: 12/05/2018
ms.keywords: GetStreamIdentifier, GetStreamIdentifier method [Media Foundation], GetStreamIdentifier method [Media Foundation],IMFStreamDescriptor interface, IMFStreamDescriptor interface [Media Foundation],GetStreamIdentifier method, IMFStreamDescriptor.GetStreamIdentifier, IMFStreamDescriptor::GetStreamIdentifier, d282ee48-6145-4557-8fa7-786b893327fa, mf.imfstreamdescriptor_getstreamidentifier, mfidl/IMFStreamDescriptor::GetStreamIdentifier
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFStreamDescriptor::GetStreamIdentifier
 - mfidl/IMFStreamDescriptor::GetStreamIdentifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFStreamDescriptor.GetStreamIdentifier
---

# IMFStreamDescriptor::GetStreamIdentifier


## -description

Retrieves an identifier for the stream.

## -parameters

### -param pdwStreamIdentifier [out]

Receives the stream identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The stream identifier uniquely identifies a stream within a presentation. It does not change throughout the lifetime of the stream. For example, if the presentation changes while the source is running, the index number of the stream may change, but the stream identifier does not.

In general, stream identifiers do not have a specific meaning, other than to identify the stream. Some media sources may assign stream identifiers based on meaningful values, such as packet identifiers, but this depends on the implementation.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor">IMFStreamDescriptor</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>