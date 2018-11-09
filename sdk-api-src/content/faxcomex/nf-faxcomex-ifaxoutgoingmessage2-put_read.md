---
UID: NF:faxcomex.IFaxOutgoingMessage2.put_Read
title: IFaxOutgoingMessage2::put_Read
author: windows-sdk-content
description: Indicates if the fax has been read.
old-location: fax\_mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_read_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingmessage2\read.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxOutgoingMessage2 interface [Fax Service],Read property, IFaxOutgoingMessage2.Read, IFaxOutgoingMessage2.get_Read, IFaxOutgoingMessage2.put_Read, IFaxOutgoingMessage2::Read, IFaxOutgoingMessage2::get_Read, IFaxOutgoingMessage2::put_Read, Read property [Fax Service], Read property [Fax Service],IFaxOutgoingMessage2 interface, _mfax_faxoutgoingmessage.read, fax._mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_read_cpp, fax._mfax_faxoutgoingmessage_read, faxcomex/IFaxOutgoingMessage2::Read, faxcomex/IFaxOutgoingMessage2::get_Read, faxcomex/IFaxOutgoingMessage2::put_Read, put_Read
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxOutgoingMessage2.Read
 - IFaxOutgoingMessage2.get_Read
 - IFaxOutgoingMessage2.put_Read
 - IFaxOutgoingMessage2.get_Read
 - IFaxOutgoingMessage2.put_Read
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingMessage2::put_Read


## -description


Indicates if the fax has been read. 


<div class="alert"><b>Note</b>  This property is supported only on Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



Possible values are VARIANT_TRUE and VARIANT_FALSE.

A change to this value is not committed to the server until <a href="https://msdn.microsoft.com/e0492e6e-db3e-449c-b58b-ff365d80d5f7">IFaxOutgoingMessage2::Save</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/fb06254f-f37b-4783-b4fd-42b5c5a28496">FaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/c6468db0-ea8d-4460-b389-43608337bd96">IFaxOutgoingMessage2</a>
 

 

