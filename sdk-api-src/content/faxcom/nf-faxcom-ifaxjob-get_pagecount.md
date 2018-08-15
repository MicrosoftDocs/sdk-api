---
UID: NF:faxcom.IFaxJob.get_PageCount
title: IFaxJob::get_PageCount
author: windows-sdk-content
description: The PageCount property is a number that represents the total number of pages in a fax transmission. The PageCount property applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_get_pagecount_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0nlg.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxJob object [Fax Service],PageCount property, FaxJob.PageCount, IFaxJob.get_PageCount, IFaxJob::get_PageCount, PageCount property [Fax Service], PageCount property [Fax Service],FaxJob object, _mfax_ifaxjob_get_pagecount, fax._mfax_ifaxjob_get_pagecount, fax._mfax_ifaxjob_get_pagecount_vb, get_PageCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxJob.PageCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_PageCount


## -description


The <b>PageCount</b> property is a number that represents the total number of pages in a fax transmission. The <b>PageCount</b> property applies only to outgoing fax transmissions.

This property is read-only.


## -parameters


## -remarks



The total page count is only available for faxes where <a href="https://msdn.microsoft.com/04d3f8e2-cf49-4497-bf89-7b9f777923b2">Type</a> returns JT_SEND. If the page count is not available, <b>PageCount</b> returns zero.

The total page count is only available for faxes that have a <a href="https://msdn.microsoft.com/04d3f8e2-cf49-4497-bf89-7b9f777923b2">Type</a> property equal to JT_SEND. If the page count is not available, the <b>PageCount</b> property is zero.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690298(v=VS.85).aspx">FaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/04d3f8e2-cf49-4497-bf89-7b9f777923b2">Type</a>
 

 

