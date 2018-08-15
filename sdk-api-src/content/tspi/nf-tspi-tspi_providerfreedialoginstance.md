---
UID: NF:tspi.TSPI_providerFreeDialogInstance
title: TSPI_providerFreeDialogInstance function
author: windows-sdk-content
description: The TSPI_providerFreeDialogInstance function informs the service provider that the dialog box associated with hdDlgInst has exited.
old-location: tspi\tspi_providerfreedialoginstance.htm
old-project: tapi
ms.assetid: 0408c43f-cb80-4caf-ab28-5ece4b2e4851
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_providerFreeDialogInstance, TSPI_providerFreeDialogInstance function [TAPI 2.2], _tspi_tspi_providerfreedialoginstance, tspi.tspi_providerfreedialoginstance, tspi/TSPI_providerFreeDialogInstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tspi.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_providerFreeDialogInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_providerFreeDialogInstance function


## -description


The 
<b>TSPI_providerFreeDialogInstance</b> function informs the service provider that the dialog box associated with <i>hdDlgInst</i> has exited. After this function is called, the service provider should no longer send data to the dialog box using 
<a href="https://msdn.microsoft.com/d3c176ba-8b4b-4b7c-a603-130dfa761898">LINE_SENDDIALOGINSTANCEDATA</a> messages.

Implementation of this function is optional; it is needed only if the service provider generates spontaneous dialog boxes in application contexts using 
<a href="https://msdn.microsoft.com/5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75">LINE_CREATEDIALOGINSTANCE</a>.


## -parameters




### -param hdDlgInst

The opaque identifier of the association between the service provider and the dialog box in the application's context, which was passed as the <b>hdDlgInstance</b> member in the 
<a href="https://msdn.microsoft.com/4de0ee9b-0643-4eab-b100-ee7aaa0b6992">TUISPICREATEDIALOGINSTANCEPARAMS</a> structure with the LINE_CREATEDIALOGINSTANCE message that created the dialog box.


## -returns



Returns zero if successful, or one of these negative error values:

LINEERR_INVALPARAM, LINEERR_NOMEM, LINEERR_OPERATIONFAILED.




## -see-also




<a href="https://msdn.microsoft.com/5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75">LINE_CREATEDIALOGINSTANCE</a>



<a href="https://msdn.microsoft.com/d3c176ba-8b4b-4b7c-a603-130dfa761898">LINE_SENDDIALOGINSTANCEDATA</a>



<a href="https://msdn.microsoft.com/4de0ee9b-0643-4eab-b100-ee7aaa0b6992">TUISPICREATEDIALOGINSTANCEPARAMS</a>
 

 

