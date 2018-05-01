---
UID: NF:wiautil.CWiauFormatConverter.ConvertToBmp
title: CWiauFormatConverter::ConvertToBmp method
author: windows-driver-content
description: The CWiauFormatConverter::ConvertToBmp method converts an image to BMP format.
old-location: image\cwiauformatconverter_converttobmp.htm
old-project: image
ms.assetid: 9ac85fe9-bc44-4a70-9619-bb13e878bb49
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiauFormatConverter, CWiauFormatConverter interface [Imaging Devices], ConvertToBmp method, CWiauFormatConverter::ConvertToBmp, ConvertToBmp method [Imaging Devices], ConvertToBmp method [Imaging Devices], CWiauFormatConverter interface, ConvertToBmp,CWiauFormatConverter.ConvertToBmp, image.cwiauformatconverter_converttobmp, wiauFncs_2c929e01-3e1f-4a07-9f2f-f50775b39017.xml, wiautil/CWiauFormatConverter::ConvertToBmp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiautil.h
req.include-header: Wiautil.h, Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiautil.h
api_name:
-	CWiauFormatConverter.ConvertToBmp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiauFormatConverter::ConvertToBmp method


## -description


The <b>CWiauFormatConverter::ConvertToBmp</b> method converts an image to BMP format.


## -parameters




### -param pSource

Points to the memory location containing the first byte of the source image.


### -param iSourceSize

Specifies the size, in bytes, of the source image.


### -param ppDest

Pointer to a memory location that receives the address of the resulting image.


### -param piDestSize

Pointer to a memory location that receives the size, in bytes, of the resulting image.


### -param pBmpImageInfo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539403">BMP_IMAGE_INFO</a> structure that receives information about the resulting image.


### -param iSkipAmt






#### - iSkipAmt = SKIP_OFF

<i>Optional</i>. Specifies the amount of the BMP header to skip. The default value of this parameter denotes that none of the BMP header is skipped.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error.




## -remarks



The caller of this method can pass a result buffer in <i>ppDest</i> and the size in <i>piDestSize</i>. Alternatively, the caller can set *<i>ppDest</i> to <b>NULL</b> and *<i>piDestSize</i> to zero in the call to indicate that this method should allocate the memory. The caller is responsible for freeing the memory using the <b>delete []</b> operator.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539403">BMP_IMAGE_INFO</a>



<a href="https://msdn.microsoft.com/b30c3336-ddc6-459d-97c4-244ca0b50cfc">CWiauFormatConverter</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540379">CWiauFormatConverter::IsFormatSupported</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548221">SKIP_AMOUNT</a>
 

 

