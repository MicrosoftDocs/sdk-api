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

# LPCQADDPAGESPROC callback function


## -description


The <b>CQAddPagesProc</b> callback function is called by a query form extension to add a page to a query form in the query dialog box. A pointer to this function is supplied to the query form extension in the <i>pAddPagesProc</i> parameter of the <a href="https://msdn.microsoft.com/797496fd-67db-4ec2-beec-224664d5d330">IQueryForm::AddPages</a> method. <b>CQAddPagesProc</b> is a placeholder for the query handler-defined function name.


## -parameters




### -param lParam

Contains a 32-bit value defined by the query handler. This value is passed to the query form extension as the <i>lParam</i> parameter in the <a href="https://msdn.microsoft.com/797496fd-67db-4ec2-beec-224664d5d330">IQueryForm::AddPages</a> call.


### -param clsidForm

Contains the <b>CLSID</b> of the form that the page should be added to. This member can contain the <b>CLSID</b> of a custom query form or one of the system-supplied forms defined for the <b>clsidDefaultForm</b> member of the <a href="https://msdn.microsoft.com/07ef2af1-230e-41d9-ad19-d002d0579d66">OPENQUERYWINDOW</a> structure.


### -param pPage

Pointer to a <a href="https://msdn.microsoft.com/09e407a2-7a58-483d-8422-4ae40c05b742">CQPAGE</a> structure that defines the page to be added.


## -returns



Returns an <b>HRESULT</b> value that indicates the success or failure of the page add operation. The following list lists possible return values.




## -see-also




<a href="https://msdn.microsoft.com/09e407a2-7a58-483d-8422-4ae40c05b742">CQPAGE</a>



<a href="https://msdn.microsoft.com/797496fd-67db-4ec2-beec-224664d5d330">IQueryForm::AddPages</a>



<a href="https://msdn.microsoft.com/07ef2af1-230e-41d9-ad19-d002d0579d66">OPENQUERYWINDOW</a>
 

 

