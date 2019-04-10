---
UID: NF:faxcom.IFaxJobs.get_Count
title: IFaxJobs::get_Count (faxcom.h)
author: windows-sdk-content
description: The IFaxJobs::get_Count method returns the number of queued fax jobs associated with the connected fax server.
old-location: fax\_mfax_ifaxjobs_get_count.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_33zo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxJobs interface [Fax Service],get_Count method, IFaxJobs.get_Count, IFaxJobs::get_Count, _mfax_ifaxjobs_get_count, fax._mfax_ifaxjobs_get_count, faxcom/IFaxJobs::get_Count, get_Count, get_Count method [Fax Service], get_Count method [Fax Service],IFaxJobs interface
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
 - IFaxJobs.get_Count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJobs::get_Count


## -description


The <b>IFaxJobs::get_Count</b> method returns the number of queued fax jobs associated with the connected fax server.


## -parameters




### -param pVal [out]

Type: <b>LONG*</b>

A pointer to a <b>LONG</b> that receives the number of fax jobs associated with the connected fax server. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After calling the <b>IFaxJobs::get_Count</b> method, a fax client application can call the <a href="https://msdn.microsoft.com/en-us/library/ms691271(v=VS.85).aspx">IFaxJobs::get_Item</a> method to retrieve interface pointers to one or more <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> objects. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692836(v=VS.85).aspx">GetJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691271(v=VS.85).aspx">IFaxJobs::get_Item</a>
 

 

