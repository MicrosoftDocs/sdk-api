---
UID: NF:faxcom.IFaxJob.get_SenderName
title: IFaxJob::get_SenderName
author: windows-sdk-content
description: The SenderName property is a null-terminated string that contains the name of the sender who initiated the fax job. The SenderName property applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxjob_get_sendername_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2vj9.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxJob object [Fax Service],SenderName property, FaxJob.SenderName, IFaxJob.get_SenderName, IFaxJob::get_SenderName, SenderName property [Fax Service], SenderName property [Fax Service],FaxJob object, _mfax_ifaxjob_get_sendername, fax._mfax_ifaxjob_get_sendername, fax._mfax_ifaxjob_get_sendername_vb, get_SenderName
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
 - FaxJob.SenderName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_SenderName


## -description


The <b>SenderName</b> property is a null-terminated string that contains the name of the sender who initiated the fax job. The <b>SenderName</b> property applies only to outgoing fax transmissions.

This property is read-only.


## -parameters


## -remarks



If the sender's name is not available, the <b>SenderName</b> property contains an empty string.

You can call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn997357">UserName</a> method to retrieve the name of the account that queued the fax job. 

<b>SenderName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690298(v=VS.85).aspx">FaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn997357">UserName</a>
 

 

