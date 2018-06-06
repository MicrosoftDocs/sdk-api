---
UID: NF:faxcomex.IFaxRecipients.get_Item
title: IFaxRecipients::get_Item
author: windows-sdk-content
description: The Item method returns a FaxRecipient object from the FaxRecipients collection.
old-location: fax\_mfax_faxrecipients_item_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0q7h_cpp.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxRecipients interface [Fax Service],get_Item method, IFaxRecipients.get_Item, IFaxRecipients::get_Item, _mfax_faxrecipients.item_cpp, fax._mfax_faxrecipients_item_cpp, faxcomex/IFaxRecipients::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxRecipients interface
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
 - IFaxRecipients.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRecipients::get_Item


## -description


The <a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a> method returns a <a href="https://msdn.microsoft.com/e418dbaf-9b07-40a9-bab8-7b4561b63325">FaxRecipient</a> object from the <a href="https://msdn.microsoft.com/b0210d82-5d62-4192-a05c-455c9f3adf9b">FaxRecipients</a> collection. 


## -parameters




### -param lIndex [in]

Type: <b>LONG</b>

A <b>LONG</b> value that specifies the item to retrieve from the fax recipient collection. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of recipients returned by a call to the <a href="https://msdn.microsoft.com/5607cb79-c790-40b9-bf3a-8c4e19dd136b">IFaxRecipients::get_Count</a> method. 


### -param ppFaxRecipient [out, retval]

Type: <b><a href="https://msdn.microsoft.com/2c8073de-644e-4594-8e52-49d07e82d432">IFaxRecipient</a>**</b>

Address of a pointer to a <a href="https://msdn.microsoft.com/2c8073de-644e-4594-8e52-49d07e82d432">IFaxRecipient</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/82a9e599-35d3-4fca-954f-dbc579c023f5">Broadcasting a Fax</a>



<a href="https://msdn.microsoft.com/b0210d82-5d62-4192-a05c-455c9f3adf9b">FaxRecipients</a>



<a href="https://msdn.microsoft.com/b2481702-3e83-4b99-87ba-d9af9fdd63aa">IFaxRecipients</a>
 

 

