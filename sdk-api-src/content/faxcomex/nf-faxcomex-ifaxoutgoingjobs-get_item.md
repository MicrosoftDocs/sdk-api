---
UID: NF:faxcomex.IFaxOutgoingJobs.get_Item
title: IFaxOutgoingJobs::get_Item
author: windows-driver-content
description: The IFaxOutgoingJobs::get_Item method returns a IFaxOutgoingJob interface from the IFaxOutgoingJobs interface.
old-location: fax\_mfax_faxoutgoingjobs_item_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_63ot_cpp.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFaxOutgoingJobs interface [Fax Service],get_Item method, IFaxOutgoingJobs.get_Item, IFaxOutgoingJobs::get_Item, _mfax_faxoutgoingjobs.item_cpp, fax._mfax_faxoutgoingjobs_item_cpp, faxcomex/IFaxOutgoingJobs::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxOutgoingJobs interface
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
-	IFaxOutgoingJobs.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutgoingJobs::get_Item


## -description


The <b>IFaxOutgoingJobs::get_Item</b> method returns a <a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a> interface from the <a href="https://msdn.microsoft.com/0d666ce6-b027-4650-8835-eac445b376a9">IFaxOutgoingJobs</a> interface.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>

Variant that specifies the item to retrieve from the collection.
				



If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. The index is 1-based. If this parameter is type VT_BSTR, the parameter is a job ID that specifies the outbound job to retrieve. Other types are not supported.


### -param pFaxOutgoingJob [out, retval]

Type: <b><a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a>**</b>

An address of a pointer that receives a <a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cfd8e842-838e-41d7-97c0-e75be908c5a0">FaxOutgoingJobs</a>



<a href="https://msdn.microsoft.com/0d666ce6-b027-4650-8835-eac445b376a9">IFaxOutgoingJobs</a>



<a href="https://msdn.microsoft.com/5fab26c3-99f6-4740-9899-3dccbd26a3ba">Visual Basic Example</a>
 

 

