---
UID: NF:faxcomex.IFaxOutgoingJobs.get__NewEnum
title: IFaxOutgoingJobs::get__NewEnum
author: windows-sdk-content
description: The IFaxOutgoingJobs::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the IFaxOutgoingJobs collection.
old-location: fax\_mfax_ifaxoutgoingjobs_get__newenum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_306l.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxOutgoingJobs interface [Fax Service],get__NewEnum method, IFaxOutgoingJobs.get__NewEnum, IFaxOutgoingJobs::get__NewEnum, _mfax_ifaxoutgoingjobs_get__newenum, fax._mfax_ifaxoutgoingjobs_get__newenum, faxcomex/IFaxOutgoingJobs::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxOutgoingJobs interface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingJobs::get__NewEnum


## -description


The <b>IFaxOutgoingJobs::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/0d666ce6-b027-4650-8835-eac445b376a9">IFaxOutgoingJobs</a> collection.


## -parameters




### -param ppUnk [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for this collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cfd8e842-838e-41d7-97c0-e75be908c5a0">FaxOutgoingJobs</a>



<a href="https://msdn.microsoft.com/0d666ce6-b027-4650-8835-eac445b376a9">IFaxOutgoingJobs</a>
 

 

