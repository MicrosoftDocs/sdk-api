---
UID: NF:faxcom.IFaxJob.get_PageCount
title: IFaxJob::get_PageCount
author: windows-sdk-content
description: The IFaxJob::get_PageCount property is a number that represents the total number of pages in a fax transmission. The IFaxJob::get_PageCount property applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_pagecount_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0nlg.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxJob interface [Fax Service],PageCount property, IFaxJob.PageCount, IFaxJob.get_PageCount, IFaxJob::PageCount, IFaxJob::get_PageCount, PageCount property [Fax Service], PageCount property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_pagecount, fax._mfax_ifaxjob_get_pagecount, fax._mfax_ifaxjob_mfax_ifaxjob_get_pagecount_cpp, faxcom/IFaxJob::PageCount, faxcom/IFaxJob::get_PageCount, get_PageCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxJob.PageCount
 - IFaxJob.get_PageCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::get_PageCount


## -description


The <b>IFaxJob::get_PageCount</b> property is a number that represents the total number of pages in a fax transmission. The <b>IFaxJob::get_PageCount</b> property applies only to outgoing fax transmissions.

This property is read-only.


## -parameters


## -remarks



The total page count is only available for faxes where <a href="https://msdn.microsoft.com/9c27ffde-ce52-4ef2-8f41-1a92884926bc">IFaxJob::get_Type</a> returns JT_SEND. If the page count is not available, <b>IFaxJob::get_PageCount</b> returns zero.

The total page count is only available for faxes that have a <a href="https://msdn.microsoft.com/9c27ffde-ce52-4ef2-8f41-1a92884926bc">IFaxJob::get_Type</a> property equal to JT_SEND. If the page count is not available, the <b>IFaxJob::get_PageCount</b> property is zero.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/9c27ffde-ce52-4ef2-8f41-1a92884926bc">IFaxJob::get_Type</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>
 

 

