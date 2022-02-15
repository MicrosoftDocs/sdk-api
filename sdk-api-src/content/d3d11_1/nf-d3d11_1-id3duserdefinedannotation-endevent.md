---
UID: NF:d3d11_1.ID3DUserDefinedAnnotation.EndEvent
title: ID3DUserDefinedAnnotation::EndEvent (d3d11_1.h)
description: Marks the end of a section of event code.
helpviewer_keywords: ["EndEvent","EndEvent method [Direct3D 11]","EndEvent method [Direct3D 11]","ID3DUserDefinedAnnotation interface","ID3DUserDefinedAnnotation interface [Direct3D 11]","EndEvent method","ID3DUserDefinedAnnotation.EndEvent","ID3DUserDefinedAnnotation::EndEvent","d3d11_1/ID3DUserDefinedAnnotation::EndEvent","direct3d11.id3duserdefinedannotation_endevent"]
old-location: direct3d11\id3duserdefinedannotation_endevent.htm
tech.root: direct3d11
ms.assetid: 5C478278-EC05-4214-80F9-808EADA76E41
ms.date: 12/05/2018
ms.keywords: EndEvent, EndEvent method [Direct3D 11], EndEvent method [Direct3D 11],ID3DUserDefinedAnnotation interface, ID3DUserDefinedAnnotation interface [Direct3D 11],EndEvent method, ID3DUserDefinedAnnotation.EndEvent, ID3DUserDefinedAnnotation::EndEvent, d3d11_1/ID3DUserDefinedAnnotation::EndEvent, direct3d11.id3duserdefinedannotation_endevent
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3DUserDefinedAnnotation::EndEvent
 - d3d11_1/ID3DUserDefinedAnnotation::EndEvent
dev_langs:
 - c++
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
---

# ID3DUserDefinedAnnotation::EndEvent


## -description

Marks the end of a section of event code.



## -returns

Returns the number of previous calls to the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3duserdefinedannotation-beginevent">ID3DUserDefinedAnnotation::BeginEvent</a> method that have not yet been finalized by calls to <b>EndEvent</b>.

The return value is –1 if the calling application is not running under a Direct3D profiling tool.

## -remarks

You call the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3duserdefinedannotation-beginevent">BeginEvent</a> method to mark the beginning of the section of event code.

A user can visualize the event when the calling application is running under an enabled Direct3D profiling tool such as Microsoft Visual Studio Ultimate 2012.

<b>EndEvent</b> has no effect if the calling application is not running under an enabled Direct3D profiling tool.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation">ID3DUserDefinedAnnotation</a>
