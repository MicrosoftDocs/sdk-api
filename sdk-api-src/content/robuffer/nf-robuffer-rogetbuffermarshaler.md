---
UID: NF:robuffer.RoGetBufferMarshaler
title: RoGetBufferMarshaler function (robuffer.h)
author: windows-sdk-content
description: Provides a standard IBuffer marshaler to implement the semantics associated with the IBuffer interface when it is marshaled.
old-location: winrt\rogetbuffermarshaler.htm
tech.root: WinRT
ms.assetid: 7F40FDC9-C6CF-44C3-AC30-EA56AB72E635
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RoGetBufferMarshaler, RoGetBufferMarshaler function [Windows Runtime], robuffer/RoGetBufferMarshaler, winrt.rogetbuffermarshaler
ms.topic: function
req.header: robuffer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wintypes.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wintypes.dll
 - API-MS-Win-Core-Winrt-robuffer-l1-1-0.dll
api_name:
 - RoGetBufferMarshaler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RoGetBufferMarshaler function


## -description


Provides a standard IBuffer marshaler to implement the semantics associated with the IBuffer interface when it is marshaled.


## -parameters




### -param bufferMarshaler [out]

pointer to Windows Runtime IBuffer marshaler


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Provided for Windows Runtime language projections.

Custom IBuffer implementations are expected to be marshaled so that the remote instance eventually copies its contents back to the original instance. The <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> implementation provided by this method handles the copy by marshaling the current value of the IBuffer and specifying a platform-provided unmarshal COM class that creates an instance with identical IBuffer contents, length, and capacity.  

The <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> implementation clones its contents to the original instance when the caller sets the Length property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>
 

 

