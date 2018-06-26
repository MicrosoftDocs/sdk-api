---
UID: NF:mmcobj.Document.Close
title: Document::Close
author: windows-sdk-content
description: The Close method closes the document.
old-location: mmc\document_close.htm
old-project: MMC
ms.assetid: 3ff35bc9-e2dc-403c-b4f3-93d1e45d98a4
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: Close, Close method [MMC], Close method [MMC],Document interface, Close method [MMC],Document object, Document interface [MMC],Close method, Document object [MMC],Close method, Document.Close, Document::Close, _slate_document.close_method, mmc.document_close
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MMCObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_PROPERTY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.exe
api_name:
 - Document.Close
 - Document.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmc.exe
req.irql: 
req.product: GDI+ 1.1
---

# Document::Close


## -description


The 
<b>Close</b> method closes the document.


## -parameters




### -param SaveChanges

Value specifying whether changes (if any) to the document should be saved. If this parameter is 1, the document is saved before it is closed; the user will not have another opportunity to save the document, although the user will be prompted (by a user interface) to provide a file name if required. If this parameter is 0, the document is closed without being saved.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/8ff15be0-6069-4862-b89f-6bce1426ce8b">Application.OnDocumentClose</a>



<a href="https://msdn.microsoft.com/658a6f9b-50ae-4bd1-9223-bed97b272770">Document.IsSaved</a>



<a href="https://msdn.microsoft.com/571941f1-bfd0-4b26-83e7-f9ab897280e7">Document.Save</a>
 

 

