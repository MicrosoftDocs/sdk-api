---
UID: NE:msinkaut.InkExtractFlags
title: InkExtractFlags
author: windows-driver-content
description: Determines how a stroke is removed from an InkDisp object.
old-location: tablet\inkextractflags.htm
old-project: tablet
ms.assetid: 22dd44bb-2175-420f-b5fd-4648ebe489a5
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: 22dd44bb-2175-420f-b5fd-4648ebe489a5, IEF_CopyFromOriginal, IEF_Default, IEF_RemoveFromOriginal, InkExtractFlags, InkExtractFlags enumeration [Tablet PC], msinkaut/IEF_CopyFromOriginal, msinkaut/IEF_Default, msinkaut/IEF_RemoveFromOriginal, msinkaut/InkExtractFlags, tablet.inkextractflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InkExtractFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	msinkaut.h
api_name:
-	InkExtractFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# InkExtractFlags enumeration


## -description



Determines how a stroke is removed from an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.




## -enum-fields




### -field IEF_CopyFromOriginal

The ink is copied from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


### -field IEF_RemoveFromOriginal

The ink is cut from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


### -field IEF_Default

The ink is cut from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


## -remarks



This enumeration is a flag.




## -see-also




<a href="https://msdn.microsoft.com/1cb109e5-5193-4022-a3b1-ade9be1337e8">ExtractStrokes Method</a>



<a href="https://msdn.microsoft.com/b32467a8-a677-4a80-8029-d364e6e372c6">ExtractWithRectangle Method</a>
 

 

