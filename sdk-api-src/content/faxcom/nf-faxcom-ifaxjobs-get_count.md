---
UID: NF:faxcom.IFaxJobs.get_Count
title: IFaxJobs::get_Count
author: windows-sdk-content
description: The IFaxJobs::get_Count method returns the number of queued fax jobs associated with the connected fax server.
old-location: fax\_mfax_ifaxjobs_get_count.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_33zo.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxJobs interface [Fax Service],get_Count method, IFaxJobs.get_Count, IFaxJobs::get_Count, _mfax_ifaxjobs_get_count, fax._mfax_ifaxjobs_get_count, faxcom/IFaxJobs::get_Count, get_Count, get_Count method [Fax Service], get_Count method [Fax Service],IFaxJobs interface
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
 - IFaxJobs.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
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



After calling the <b>IFaxJobs::get_Count</b> method, a fax client application can call the <a href="https://msdn.microsoft.com/1279c69b-42b0-4ce2-92e1-307d3d7999b4">IFaxJobs::get_Item</a> method to retrieve interface pointers to one or more <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> objects. 




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/45b195f9-0ac9-4150-84cf-64049cc4053f">GetJobs</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>



<a href="https://msdn.microsoft.com/1279c69b-42b0-4ce2-92e1-307d3d7999b4">IFaxJobs::get_Item</a>
 

 

