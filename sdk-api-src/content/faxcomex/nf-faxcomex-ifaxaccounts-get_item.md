---
UID: NF:faxcomex.IFaxAccounts.get_Item
title: IFaxAccounts::get_Item
author: windows-sdk-content
description: Returns a FaxAccount object from a FaxAccounts collection.
old-location: fax\_mfax_faxaccounts_item_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccounts\get_item.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxAccounts interface [Fax Service],get_Item method, IFaxAccounts.get_Item, IFaxAccounts::get_Item, _mfax_faxaccounts.item_cpp, fax._mfax_faxaccounts_item_cpp, faxcomex/IFaxAccounts::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxAccounts interface
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxAccounts.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxAccounts::get_Item


## -description


Returns a <a href="https://msdn.microsoft.com/85adc440-3dc8-47ce-aae8-dfb04f824b09">FaxAccount</a> object from a <a href="https://msdn.microsoft.com/bf26e82e-af97-43a1-81be-1bcb61b6cf98">FaxAccounts</a> collection. 


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies a value that indicates the item to retrieve from the collection. If this parameter is type <b>VT_I2</b> or <b>VT_I4</b>, it specifies the index of the item to retrieve. The index is 1-based. If this parameter is type <b>VT_BSTR</b>, it specifies the account name to use to search the collection. Other types are not supported. 


### -param pFaxAccount






#### - ppFaxAccount [out, retval]

Type: <b><a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a>**</b>

The <a href="https://msdn.microsoft.com/85adc440-3dc8-47ce-aae8-dfb04f824b09">FaxAccount</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73210bf5-cae8-4fea-802a-a37f59a1dd2f">IFaxAccounts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
 

 

