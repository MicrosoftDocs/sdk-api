---
UID: NF:cmnquery.IQueryForm.AddPages
title: IQueryForm::AddPages
author: windows-sdk-content
description: Called to allow a query form object to add pages to an existing form.
old-location: ad\iqueryform_addpages.htm
tech.root: ad
ms.assetid: 797496fd-67db-4ec2-beec-224664d5d330
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: AddPages, AddPages method [Active Directory], AddPages method [Active Directory],IQueryForm interface, IQueryForm interface [Active Directory],AddPages method, IQueryForm.AddPages, IQueryForm::AddPages, _glines_iqueryform_addpages, ad.iqueryform__addpages, ad.iqueryform_addpages, cmnquery/IQueryForm::AddPages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - IQueryForm.AddPages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQueryForm::AddPages


## -description


The <b>IQueryForm::AddPages</b> method is called to allow a query form object to add pages to an existing form.


## -parameters




### -param pAddPagesProc [in]

Pointer to a callback function of the form <a href="https://msdn.microsoft.com/2b62c1aa-ace7-4083-8eb3-7c5c499762c9">CQAddPagesProc</a>. The query form extension  calls this function with the supplied <i>lParam</i> one time for each page to be added to a form.


### -param lParam [in]

Contains a 32-bit value that is defined by the query handler. This value must be passed as the <i>lParam</i> parameter in the <a href="https://msdn.microsoft.com/2b62c1aa-ace7-4083-8eb3-7c5c499762c9">CQAddPagesProc</a> call.


## -returns



Returns <b>S_OK</b> if successful or a standard <b>HRESULT</b> failure code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/2b62c1aa-ace7-4083-8eb3-7c5c499762c9">CQAddPagesProc</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/fd4f41f0-8aeb-4c83-a079-a5a77685c143">IQueryForm</a>
 

 

