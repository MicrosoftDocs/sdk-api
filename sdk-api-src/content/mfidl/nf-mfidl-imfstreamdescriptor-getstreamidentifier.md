---
UID: NF:mfidl.IMFStreamDescriptor.GetStreamIdentifier
title: IMFStreamDescriptor::GetStreamIdentifier
author: windows-sdk-content
description: Retrieves an identifier for the stream.
old-location: mf\imfstreamdescriptor_getstreamidentifier.htm
old-project: medfound
ms.assetid: d282ee48-6145-4557-8fa7-786b893327fa
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetStreamIdentifier, GetStreamIdentifier method [Media Foundation], GetStreamIdentifier method [Media Foundation],IMFStreamDescriptor interface, IMFStreamDescriptor interface [Media Foundation],GetStreamIdentifier method, IMFStreamDescriptor.GetStreamIdentifier, IMFStreamDescriptor::GetStreamIdentifier, d282ee48-6145-4557-8fa7-786b893327fa, mf.imfstreamdescriptor_getstreamidentifier, mfidl/IMFStreamDescriptor::GetStreamIdentifier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFStreamDescriptor.GetStreamIdentifier
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFStreamDescriptor::GetStreamIdentifier


## -description



Retrieves an identifier for the stream.




## -parameters




### -param pdwStreamIdentifier [out]

Receives the stream identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The stream identifier uniquely identifies a stream within a presentation. It does not change throughout the lifetime of the stream. For example, if the presentation changes while the source is running, the index number of the stream may change, but the stream identifier does not.

In general, stream identifiers do not have a specific meaning, other than to identify the stream. Some media sources may assign stream identifiers based on meaningful values, such as packet identifiers, but this depends on the implementation.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a076dc6e-d9cb-4f7e-8cc2-b66292da295f">IMFStreamDescriptor</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

