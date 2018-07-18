---
UID: NF:faxcomex.IFaxDevices.get__NewEnum
title: IFaxDevices::get__NewEnum
author: windows-sdk-content
description: The IFaxDevices::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the FaxDevices collection.
old-location: fax\_mfax_ifaxdevices_get__newenum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2iel.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IFaxDevices interface [Fax Service],get__NewEnum method, IFaxDevices.get__NewEnum, IFaxDevices::get__NewEnum, _mfax_ifaxdevices_get__newenum, fax._mfax_ifaxdevices_get__newenum, faxcomex/IFaxDevices::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxDevices interface
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
 - IFaxDevices.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDevices::get__NewEnum


## -description


The <b>IFaxDevices::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection.


## -parameters




### -param ppUnk [out, retval]

Type: <b><a href="_com_IUnknown">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="_com_IUnknown">IUnknown</a> interface for the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Microsoft Visual Basic, you do not need to use the <b>_NewEnum</b> property, because it is automatically used in the implementation of <b>For Each ... Next</b>.




## -see-also




<a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a>



<a href="https://msdn.microsoft.com/025b7393-b693-4d75-973a-4a058059eb22">IFaxDevices</a>



<a href="https://msdn.microsoft.com/422003a1-7db2-4eff-97bd-8ca889a3e5f6">Visual Basic Example</a>
 

 

