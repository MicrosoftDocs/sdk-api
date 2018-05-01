---
UID: NF:faxcomex.IFaxIncomingJobs.get_Item
title: IFaxIncomingJobs::get_Item method
author: windows-driver-content
description: Retrieves a FaxIncomingJob object from the FaxIncomingJobs collection.
old-location: fax\_mfax_faxincomingjobs_item_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5ga5_cpp.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxIncomingJobs, IFaxIncomingJobs interface [Fax Service], get_Item method, IFaxIncomingJobs::get_Item, _mfax_faxincomingjobs.item_cpp, fax._mfax_faxincomingjobs_item_cpp, faxcomex/IFaxIncomingJobs::get_Item, get_Item method [Fax Service], get_Item method [Fax Service], IFaxIncomingJobs interface, get_Item,IFaxIncomingJobs.get_Item
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
-	IFaxIncomingJobs.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingJobs::get_Item method


## -description


Retrieves a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object from the <a href="https://msdn.microsoft.com/05b2ceec-d8e9-4ee8-be0c-e31bb12edfc8">FaxIncomingJobs</a> collection.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies a value that indicates the item to retrieve from the collection. If this parameter is type <b>VT_I2</b> or <b>VT_I4</b>, it specifies the index of the item to retrieve. The index is 1-based. If this parameter is type <b>VT_BSTR</b>, it specifies a job ID to use to search the collection. Other types are not supported. 


### -param pFaxIncomingJob [out, retval]

Type: <b><a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>**</b>

Receives an indirect pointer to a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/970a6047-4c85-404d-ad7e-39703f09f856">IFaxIncomingJobs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
 

 

