---
UID: NF:faxcom.IFaxJob.get_FaxNumber
title: IFaxJob::get_FaxNumber
author: windows-sdk-content
description: The FaxNumber property is a null-terminated string that contains the fax number to which the fax server will transmit the fax job. The FaxNumber property applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_get_faxnumber_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_42wi.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxJob object [Fax Service],FaxNumber property, FaxJob.FaxNumber, FaxNumber property [Fax Service], FaxNumber property [Fax Service],FaxJob object, IFaxJob.get_FaxNumber, IFaxJob::get_FaxNumber, _mfax_ifaxjob_get_faxnumber, fax._mfax_ifaxjob_get_faxnumber, fax._mfax_ifaxjob_get_faxnumber_vb, get_FaxNumber
ms.prod: windows
ms.technology: windows-sdk
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
 - FaxJob.FaxNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_FaxNumber


## -description


The <b>FaxNumber</b> property is a null-terminated string that contains the fax number to which the fax server will transmit the fax job. The <b>FaxNumber</b> property applies only to outgoing fax transmissions.

This property is read-only.


## -parameters


## -remarks



A fax number is only available for faxes that have a <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property equal to <b>JT_SEND</b>. If the fax number is not available, the <b>FaxNumber</b> property contains an empty string.

<b>FaxNumber</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690298(v=VS.85).aspx">FaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>
 

 

