---
UID: NF:faxcomex.IFaxRecipients.get__NewEnum
title: IFaxRecipients::get__NewEnum
author: windows-driver-content
description: The IFaxRecipients::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the FaxRecipients collection.
old-location: fax\_mfax_ifaxrecipients_get__newenum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_22p9.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxRecipients interface [Fax Service],get__NewEnum method, IFaxRecipients.get__NewEnum, IFaxRecipients::get__NewEnum, _mfax_ifaxrecipients_get__newenum, fax._mfax_ifaxrecipients_get__newenum, faxcomex/IFaxRecipients::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxRecipients interface
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
-	IFaxRecipients.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRecipients::get__NewEnum


## -description


The <b>IFaxRecipients::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="https://msdn.microsoft.com/b0210d82-5d62-4192-a05c-455c9f3adf9b">FaxRecipients</a> collection.


## -parameters




### -param ppUnk [out, retval]

Type: <b><a href="_com_IUnknown">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="_com_IUnknown">IUnknown</a> interface for the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Microsoft Visual Basic, you do not need to use the <b>_NewEnum</b> property because it is automatically used in the implementation of <b>For Each ... Next</b>.




## -see-also




<a href="https://msdn.microsoft.com/b2481702-3e83-4b99-87ba-d9af9fdd63aa">IFaxRecipients</a>
 

 

