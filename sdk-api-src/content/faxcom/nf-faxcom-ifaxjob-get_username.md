---
UID: NF:faxcom.IFaxJob.get_UserName
title: IFaxJob::get_UserName
author: windows-sdk-content
description: The UserName property is a null-terminated string that contains the name of the user who submitted the fax job to the job queue. The UserName property applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_get_username_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6jad.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxJob object [Fax Service],UserName property, FaxJob.UserName, IFaxJob.get_UserName, IFaxJob::get_UserName, UserName property [Fax Service], UserName property [Fax Service],FaxJob object, _mfax_ifaxjob_get_username, fax._mfax_ifaxjob_get_username, fax._mfax_ifaxjob_get_username_vb, get_UserName
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
 - FaxJob.UserName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_UserName


## -description


The <b>UserName</b> property is a null-terminated string that contains the name of the user who submitted the fax job to the job queue. The <b>UserName</b> property applies only to outgoing fax transmissions.


This property is read-only.


## -parameters


## -remarks



You can use the <b>UserName</b> property to retrieve the name of the person who initiated the fax job.

<b>UserName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690298(v=VS.85).aspx">FaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt764038">SenderName</a>
 

 

