---
UID: NF:faxcomex.IFaxRecipients.Remove
title: IFaxRecipients::Remove
author: windows-sdk-content
description: The IFaxRecipients::Remove method removes an item from the FaxRecipients collection.
old-location: fax\_mfax_faxrecipients_cpp_mfax_faxrecipients_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9c9x.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxRecipients interface [Fax Service],Remove method, IFaxRecipients.Remove, IFaxRecipients::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxRecipients interface, _mfax_faxrecipients.remove, fax._mfax_faxrecipients_cpp_mfax_faxrecipients_remove_cpp, fax._mfax_faxrecipients_remove, faxcomex/IFaxRecipients::Remove
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
 - IFaxRecipients.Remove
 - IFaxRecipients.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxRecipients.Remove
: 
---

# IFaxRecipients::Remove


## -description


The <b>IFaxRecipients::Remove</b> method removes an item from the <a href="https://msdn.microsoft.com/b0210d82-5d62-4192-a05c-455c9f3adf9b">FaxRecipients</a> collection.


## -parameters




### -param lIndex [out, retval]

Type: <b>LONG</b>

A <b>LONG</b> that specifies the index of the item to remove from the collection. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of recipients returned by a call to the <a href="https://msdn.microsoft.com/5607cb79-c790-40b9-bf3a-8c4e19dd136b">IFaxRecipients::get_Count</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/82a9e599-35d3-4fca-954f-dbc579c023f5">Broadcasting a Fax</a>



<a href="https://msdn.microsoft.com/b0210d82-5d62-4192-a05c-455c9f3adf9b">FaxRecipients</a>



<a href="https://msdn.microsoft.com/b2481702-3e83-4b99-87ba-d9af9fdd63aa">IFaxRecipients</a>
 

 

