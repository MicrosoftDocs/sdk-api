---
UID: NF:faxcom.IFaxJobs.get_Item
title: IFaxJobs::get_Item
author: windows-sdk-content
description: The IFaxJobs::get_Item method returns a new FaxJob object for a specified fax job. The object allows enumeration of the fax jobs associated with a connected fax server.
old-location: fax\_mfax_ifaxjobs_get_item.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1zn1.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxJobs interface [Fax Service],get_Item method, IFaxJobs.get_Item, IFaxJobs::get_Item, _mfax_ifaxjobs_get_item, fax._mfax_ifaxjobs_get_item, faxcom/IFaxJobs::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxJobs interface
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
 - IFaxJobs.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxJobs::get_Item


## -description


The <b>IFaxJobs::get_Item</b> method returns a new <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object for a specified fax job. The object allows enumeration of the fax jobs associated with a connected fax server.


## -parameters




### -param Index [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the fax job to retrieve. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> objects returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691382(v=VS.85).aspx">IFaxJobs::get_Count</a> method. 


### -param pVal [out]

Type: <b>VARIANT*</b>

Receives a pointer to a <b>VARIANT</b> structure that receives an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692342(v=VS.85).aspx">FaxJob</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A fax client application can also access the <a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a> interface directly by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxJob</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692836(v=VS.85).aspx">GetJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692310(v=VS.85).aspx">IFaxJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692372(v=VS.85).aspx">IFaxJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691382(v=VS.85).aspx">IFaxJobs::get_Count</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

