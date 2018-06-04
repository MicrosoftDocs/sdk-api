---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# LPCQADDFORMSPROC callback function


## -description


The <b>CQAddFormsProc</b> callback function is called by a query form extension to add a form to the query dialog box. A pointer to this function is supplied to the query form extension in the <i>pAddFormsProc</i> parameter of the <a href="https://msdn.microsoft.com/fadaa7e6-ccf2-42cd-a26e-19db107ce56c">IQueryForm::AddForms</a> method. <b>CQAddFormsProc</b> is a placeholder for the query handler-defined function name.


## -parameters




### -param lParam

Contains a 32-bit value defined by the query handler. This value is passed to the query form extension as the <i>lParam</i> parameter in the <a href="https://msdn.microsoft.com/fadaa7e6-ccf2-42cd-a26e-19db107ce56c">IQueryForm::AddForms</a> call.


### -param pForm

Pointer to a <a href="https://msdn.microsoft.com/65cf2e9c-8f88-4e84-8bf2-2b0fd246a835">CQFORM</a> structure that defines the form to add.


## -returns



Returns an <b>HRESULT</b> value that indicates the success, or failure, of the form add operation. The following list lists possible return values.




## -see-also




<a href="https://msdn.microsoft.com/65cf2e9c-8f88-4e84-8bf2-2b0fd246a835">CQFORM</a>



<a href="https://msdn.microsoft.com/fadaa7e6-ccf2-42cd-a26e-19db107ce56c">IQueryForm::AddForms</a>
 

 

