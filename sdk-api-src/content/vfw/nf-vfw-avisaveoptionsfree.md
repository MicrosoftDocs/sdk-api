---
UID: NF:vfw.AVISaveOptionsFree
title: AVISaveOptionsFree function
author: windows-sdk-content
description: The AVISaveOptionsFree function frees the resources allocated by the AVISaveOptions function.
old-location: multimedia\avisaveoptionsfree.htm
old-project: Multimedia
ms.assetid: c88a786f-d008-4eb6-af3d-59a0f62ac09d
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: AVISaveOptionsFree, AVISaveOptionsFree function [Windows Multimedia], _win32_AVISaveOptionsFree, multimedia.avisaveoptionsfree, vfw/AVISaveOptionsFree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Avifil32.dll
api_name:
-	AVISaveOptionsFree
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVISaveOptionsFree function


## -description



The <b>AVISaveOptionsFree</b> function frees the resources allocated by the <a href="https://msdn.microsoft.com/6141272f-a815-4ba8-bc6b-41751d6e0104">AVISaveOptions</a> function.




## -parameters




### -param nStreams

Count of the <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structures referenced in <i>plpOptions</i>.


### -param plpOptions

Pointer to an array of pointers to <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structures. These structures hold the compression options set by the dialog box. The resources allocated by <a href="https://msdn.microsoft.com/6141272f-a815-4ba8-bc6b-41751d6e0104">AVISaveOptions</a> for each of these structures will be freed.


## -returns



Returns AVIERR_OK.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

