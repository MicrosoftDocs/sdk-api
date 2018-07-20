---
UID: NF:faxcom.IFaxJob.get_DisplayName
title: IFaxJob::get_DisplayName
author: windows-sdk-content
description: The DisplayName property is a null-terminated string that contains the user-friendly name to associate with the fax job.
old-location: fax\_mfax_ifaxjob_get_displayname_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8b39.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DisplayName property [Fax Service], DisplayName property [Fax Service],FaxJob object, FaxJob object [Fax Service],DisplayName property, FaxJob.DisplayName, IFaxJob.get_DisplayName, IFaxJob::get_DisplayName, _mfax_ifaxjob_get_displayname, fax._mfax_ifaxjob_get_displayname, fax._mfax_ifaxjob_get_displayname_vb, get_DisplayName
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
 - FaxJob.DisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJob::get_DisplayName


## -description


The <b>DisplayName</b> property is a null-terminated string that contains the user-friendly name to associate with the fax job.


This property is read-only.


## -parameters


## -remarks



You can use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff545145">JobId</a> property to uniquely identify a fax job because it is possible for multiple fax jobs to have the same <b>DisplayName</b> property.

<b>DisplayName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.





## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690298(v=VS.85).aspx">FaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545145">JobId</a>
 

 

