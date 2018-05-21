---
UID: NC:cmnquery.LPCQADDFORMSPROC
title: LPCQADDFORMSPROC
author: windows-driver-content
description: Called by a query form extension to add a form to the query dialog box.
old-location: ad\cqaddformsproc.htm
old-project: AD
ms.assetid: e4221299-93de-4747-b464-0d152d6e767b
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: CQAddFormsProc, CQAddFormsProc callback, CQAddFormsProc callback function [Active Directory], LPCQADDFORMSPROC, LPCQADDFORMSPROC callback function pointer [Active Directory], ad.cqaddformsproc, cmnquery/CQAddFormsProc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Cmnquery.h
api_name:
-	LPCQADDFORMSPROC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

