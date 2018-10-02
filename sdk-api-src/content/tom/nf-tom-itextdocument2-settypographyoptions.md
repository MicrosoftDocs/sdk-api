---
UID: NF:tom.ITextDocument2.SetTypographyOptions
title: ITextDocument2::SetTypographyOptions
author: windows-sdk-content
description: Specifies the typography options for the document.
old-location: controls\itextdocument2_settypographyoptions.htm
tech.root: controls
ms.assetid: 1013c9bf-b6fe-4396-b7a8-36e61edf1df3
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetTypographyOptions method, ITextDocument2.SetTypographyOptions, ITextDocument2::SetTypographyOptions, SetTypographyOptions, SetTypographyOptions method [Windows Controls], SetTypographyOptions method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_settypographyoptions, tom/ITextDocument2::SetTypographyOptions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument2.SetTypographyOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument2::SetTypographyOptions


## -description


Specifies the typography options for the document.


## -parameters




### -param Options [in]

Type: <b>long</b>

The typography options to set. For a list of possible options, see <a href="https://msdn.microsoft.com/3433954c-818b-4811-9e38-4bc8ab3ee7f9">GetTypographyOptions</a>.


### -param Mask [in]

Type: <b>long</b>

A mask identifying the options to set. For example, to turn on <b>TO_ADVANCEDTYPOGRAPHY</b>, call <b>ITextDocument2::SetTypographyOptions (TO_ADVANCEDTYPOGRAPHY, TO_ADVANCEDTYPOGRAPHY)</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/3433954c-818b-4811-9e38-4bc8ab3ee7f9">ITextDocument2::GetTypographyOptions</a>
 

 

