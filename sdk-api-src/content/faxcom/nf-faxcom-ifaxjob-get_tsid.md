---
UID: NF:faxcom.IFaxJob.get_Tsid
title: IFaxJob::get_Tsid
author: windows-sdk-content
description: The IFaxJob::get_Tsid property is a null-terminated string that contains the transmitting station identifier (TSID)) associated with the fax job.
old-location: fax\_mfax_ifaxjob_mfax_ifaxjob_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4zz8.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxJob interface [Fax Service],Tsid property, IFaxJob.Tsid, IFaxJob.get_Tsid, IFaxJob::Tsid, IFaxJob::get_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxJob interface, _mfax_ifaxjob_get_tsid, fax._mfax_ifaxjob_get_tsid, fax._mfax_ifaxjob_mfax_ifaxjob_get_tsid_cpp, faxcom/IFaxJob::Tsid, faxcom/IFaxJob::get_Tsid, get_Tsid
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
 - IFaxJob.Tsid
 - IFaxJob.get_Tsid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJob::get_Tsid


## -description


The <b>IFaxJob::get_Tsid</b> property is a null-terminated string that contains the 
transmitting station identifier (TSID)) associated with the fax job.

This property is read-only.


## -parameters


## -remarks



If the TSID is not available, <b>IFaxJob::get_Tsid</b> is an empty string. 

You can use the <a href="https://msdn.microsoft.com/a27d55e8-68c0-4700-becb-d56ecddbef44">UseDeviceTsid</a> property to determine if the fax server is configured to permit user-specified TSIDs. 

Note that the T.30 specification of the International Telecommunication Union (ITU) restricts the value of a TSID to 20 ASCII characters. If a fax client application specifies a TSID that contains non-ASCII characters, the fax service removes them. If the TSID exceeds 20 characters, the service truncates the extra characters. 

<b>IFaxJob::get_Tsid</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/a27d55e8-68c0-4700-becb-d56ecddbef44">UseDeviceTsid</a>
 

 

