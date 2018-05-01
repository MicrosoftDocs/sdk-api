---
UID: NF:faxcom.IFaxJobs.get_Item
title: IFaxJobs::get_Item method
author: windows-driver-content
description: The IFaxJobs::get_Item method returns a new FaxJob object for a specified fax job. The object allows enumeration of the fax jobs associated with a connected fax server.
old-location: fax\_mfax_ifaxjobs_get_item.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1zn1.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxJobs, IFaxJobs interface [Fax Service], get_Item method, IFaxJobs::get_Item, _mfax_ifaxjobs_get_item, fax._mfax_ifaxjobs_get_item, faxcom/IFaxJobs::get_Item, get_Item method [Fax Service], get_Item method [Fax Service], IFaxJobs interface, get_Item,IFaxJobs.get_Item
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	IFaxJobs.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxJobs::get_Item method


## -description


The <b>IFaxJobs::get_Item</b> method returns a new <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object for a specified fax job. The object allows enumeration of the fax jobs associated with a connected fax server.


## -parameters




### -param Index [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the fax job to retrieve. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> objects returned by a call to the <a href="https://msdn.microsoft.com/476d4381-30b4-4749-b1ea-fbd28ca8148d">IFaxJobs::get_Count</a> method. 


### -param pVal [out]

Type: <b>VARIANT*</b>

Receives a pointer to a <b>VARIANT</b> structure that receives an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/4c8376a4-dded-489e-a361-ce6edd0e17af">FaxJob</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A fax client application can also access the <a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a> interface directly by calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxJob</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/45b195f9-0ac9-4150-84cf-64049cc4053f">GetJobs</a>



<a href="https://msdn.microsoft.com/48de5e31-0286-4b7a-a86b-46411bf0e9e8">IFaxJob</a>



<a href="https://msdn.microsoft.com/c9e548c4-9381-4b7d-9a9d-55fbc59f198f">IFaxJobs</a>



<a href="https://msdn.microsoft.com/476d4381-30b4-4749-b1ea-fbd28ca8148d">IFaxJobs::get_Count</a>



<a href="_com_IUnknown">IUnknown</a>
 

 

