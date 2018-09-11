---
UID: NF:muiload.FreeMUILibrary
title: FreeMUILibrary function
author: windows-sdk-content
description: Releases the handle to a resource module loaded by LoadMUILibrary.
old-location: intl\freemuilibrary.htm
tech.root: Intl
ms.assetid: 38a0d7cb-46a9-449b-8f7e-4c573e400e75
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: FreeMUILibrary, FreeMUILibrary function [Internationalization for Windows Applications], _win32_FreeMUILibrary, intl.freemuilibrary, muiload/FreeMUILibrary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: muiload.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Muiload.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Muiload.lib
api_name:
 - FreeMUILibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: Muiload.lib, included in theWindows SDKforWindows VistaonWindows 2000 Professional,Windows Me/98/95.  Not supported onWindows NT 4.0
---

# FreeMUILibrary function


## -description


Releases the handle to a resource module loaded by <a href="https://msdn.microsoft.com/277067d8-c38d-4e79-9c1a-4e4af1987228">LoadMUILibrary</a>.


## -parameters




### -param hResModule [in]

Handle to a resource module loaded by <a href="https://msdn.microsoft.com/277067d8-c38d-4e79-9c1a-4e4af1987228">LoadMUILibrary</a>. The handle indicates either a language-specific resource file or an LN file.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The error code is the same as that returned by <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>.




## -remarks



Once the application has called <b>FreeMUILibrary</b>, it should treat the passed module handle as invalid.

Applications using this function can be built on pre-Windows Vista operating systems, but they must link statically with the MUILoad library provided in the Microsoft Windows SDK for Windows Vista.

<b>FreeMUILibrary</b> is related to <a href="https://msdn.microsoft.com/277067d8-c38d-4e79-9c1a-4e4af1987228">LoadMUILibrary</a> in the same way that <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> is related to <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>, and similar considerations need to be applied to its usage. In particular, to support correct reference counting, <b>FreeMUILibrary</b> should be called for any handle returned by <b>LoadMUILibrary</b>. For more information see the Remarks sections of <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> and <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>.




## -see-also




<a href="https://msdn.microsoft.com/277067d8-c38d-4e79-9c1a-4e4af1987228">LoadMUILibrary</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>
 

 

