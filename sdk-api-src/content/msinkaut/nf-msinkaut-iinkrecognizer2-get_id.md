---
UID: NF:msinkaut.IInkRecognizer2.get_Id
title: IInkRecognizer2::get_Id (msinkaut.h)
author: windows-sdk-content
description: Retrieves the ID for the InkRecognizer.
old-location: tablet\iinkrecognizer2_get_id.htm
tech.root: tablet
ms.assetid: c298634b-bf51-4c69-a183-ce6b2f8da41a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkRecognizer2 interface [Tablet PC],get_Id method, IInkRecognizer2.get_Id, IInkRecognizer2::get_Id, c298634b-bf51-4c69-a183-ce6b2f8da41a, get_Id, get_Id method [Tablet PC], get_Id method [Tablet PC],IInkRecognizer2 interface, msinkaut/IInkRecognizer2::get_Id, tablet.iinkrecognizer2_get_id
ms.topic: method
f1_keywords: ["msinkaut/IInkRecognizer2.get_Id"]
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizer2.get_Id
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognizer2::get_Id


## -description



Retrieves the ID for the InkRecognizer.




## -parameters




### -param pbstrId [out]

A BSTR containing the ID of the recognizer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To access this method, first create and instance of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>, then call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> to get a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer2">IInkRecognizer2 Interface</a>. Use this pointer to call the <b>get_Id</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer2">IInkRecognizer2 Interface</a>
 

 

