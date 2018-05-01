---
UID: NF:faxcomex.IFaxDeviceIds.get__NewEnum
title: IFaxDeviceIds::get__NewEnum method
author: windows-driver-content
description: The IFaxDeviceIds::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the FaxDeviceIds collection.
old-location: fax\_mfax_ifaxdeviceids_get__newenum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4gj1.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxDeviceIds, IFaxDeviceIds interface [Fax Service], get__NewEnum method, IFaxDeviceIds::get__NewEnum, _mfax_ifaxdeviceids_get__newenum, fax._mfax_ifaxdeviceids_get__newenum, faxcomex/IFaxDeviceIds::get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service], IFaxDeviceIds interface, get__NewEnum,IFaxDeviceIds.get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxDeviceIds.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDeviceIds::get__NewEnum method


## -description


The <b>IFaxDeviceIds::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a> collection.


## -parameters




### -param ppUnk [out, retval]

Type: <b><a href="_com_IUnknown">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="_com_IUnknown">IUnknown</a> interface for the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Microsoft Visual Basic, you do not need to use the corresponding <b>_NewEnum</b> property, because it is automatically used in the implementation of <b>For Each ... Next</b>.




## -see-also




<a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a>



<a href="https://msdn.microsoft.com/8ba11f07-3796-4910-98f7-541a32519c41">IFaxDeviceIds</a>
 

 

