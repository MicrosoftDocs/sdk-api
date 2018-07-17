---
UID: NF:msinkaut.IInkRecognizer2.get_Id
title: IInkRecognizer2::get_Id
author: windows-sdk-content
description: Retrieves the ID for the InkRecognizer.
old-location: tablet\iinkrecognizer2_get_id.htm
old-project: tablet
ms.assetid: c298634b-bf51-4c69-a183-ce6b2f8da41a
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IInkRecognizer2 interface [Tablet PC],get_Id method, IInkRecognizer2.get_Id, IInkRecognizer2::get_Id, c298634b-bf51-4c69-a183-ce6b2f8da41a, get_Id, get_Id method [Tablet PC], get_Id method [Tablet PC],IInkRecognizer2 interface, msinkaut/IInkRecognizer2::get_Id, tablet.iinkrecognizer2_get_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



To access this method, first create and instance of the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>, then call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to get a pointer to the <a href="https://msdn.microsoft.com/07a493a7-4ffc-403e-8f61-1bb8233c973e">IInkRecognizer2 Interface</a>. Use this pointer to call the <b>get_Id</b> method.




## -see-also




<a href="https://msdn.microsoft.com/07a493a7-4ffc-403e-8f61-1bb8233c973e">IInkRecognizer2 Interface</a>
 

 

