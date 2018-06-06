---
UID: NF:d3d11_1.ID3DUserDefinedAnnotation.EndEvent
title: ID3DUserDefinedAnnotation::EndEvent
author: windows-sdk-content
description: Marks the end of a section of event code.
old-location: direct3d11\id3duserdefinedannotation_endevent.htm
old-project: direct3d11
ms.assetid: 5C478278-EC05-4214-80F9-808EADA76E41
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: EndEvent, EndEvent method [Direct3D 11], EndEvent method [Direct3D 11],ID3DUserDefinedAnnotation interface, ID3DUserDefinedAnnotation interface [Direct3D 11],EndEvent method, ID3DUserDefinedAnnotation.EndEvent, ID3DUserDefinedAnnotation::EndEvent, d3d11_1/ID3DUserDefinedAnnotation::EndEvent, direct3d11.id3duserdefinedannotation_endevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3DUserDefinedAnnotation.EndEvent
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3DUserDefinedAnnotation::EndEvent


## -description


Marks the end of a section of event code.


## -parameters






## -returns



Returns the number of previous calls to the <a href="https://msdn.microsoft.com/38FC7BFA-A01E-4537-88F1-836AE03C9A07">ID3DUserDefinedAnnotation::BeginEvent</a> method that have not yet been finalized by calls to <b>EndEvent</b>.

The return value is –1 if the calling application is not running under a Direct3D profiling tool.




## -remarks



You call the <a href="https://msdn.microsoft.com/38FC7BFA-A01E-4537-88F1-836AE03C9A07">BeginEvent</a> method to mark the beginning of the section of event code.

A user can visualize the event when the calling application is running under an enabled Direct3D profiling tool such as Microsoft Visual Studio Ultimate 2012.

<b>EndEvent</b> has no effect if the calling application is not running under an enabled Direct3D profiling tool.




## -see-also




<a href="https://msdn.microsoft.com/255DE24B-3D6D-49D9-B6A8-D296AB99B4C9">ID3DUserDefinedAnnotation</a>
 

 

