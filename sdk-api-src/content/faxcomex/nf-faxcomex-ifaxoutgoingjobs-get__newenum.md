---
UID: NF:faxcomex.IFaxOutgoingJobs.get__NewEnum
title: IFaxOutgoingJobs::get__NewEnum (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingJobs::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the IFaxOutgoingJobs collection.
old-location: fax\_mfax_ifaxoutgoingjobs_get__newenum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_306l.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutgoingJobs interface [Fax Service],get__NewEnum method, IFaxOutgoingJobs.get__NewEnum, IFaxOutgoingJobs::get__NewEnum, _mfax_ifaxoutgoingjobs_get__newenum, fax._mfax_ifaxoutgoingjobs_get__newenum, faxcomex/IFaxOutgoingJobs::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxOutgoingJobs interface
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingJobs.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingJobs::get__NewEnum


## -description


The <b>IFaxOutgoingJobs::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/en-us/library/ms689507(v=VS.85).aspx">IFaxOutgoingJobs</a> collection.


## -parameters




### -param ppUnk [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface for this collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689505(v=VS.85).aspx">FaxOutgoingJobs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689507(v=VS.85).aspx">IFaxOutgoingJobs</a>
 

 

