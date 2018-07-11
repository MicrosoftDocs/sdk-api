---
UID: NF:faxcomex.IFaxAccount.get_AccountName
title: IFaxAccount::get_AccountName
author: windows-sdk-content
description: Retrieves the name of a particular fax account on the server.
old-location: fax\_mfax_faxaccount_accountname_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccount\accountname.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: AccountName property [Fax Service], AccountName property [Fax Service],FaxAccount object, FaxAccount object [Fax Service],AccountName property, FaxAccount.AccountName, IFaxAccount.get_AccountName, IFaxAccount::get_AccountName, _mfax_faxaccount.accountname, fax._mfax_faxaccount_accountname, fax._mfax_faxaccount_accountname_vb, get_AccountName
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
 - FaxAccount.AccountName
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxAccount::get_AccountName


## -description


Retrieves the name of a particular fax account on the server.

This property is read-only.


## -parameters


## -remarks



If the account is not in the local domain, the format of name returned  is &lt;domain_name&gt;\&lt;user_name&gt;.

If the account is in the domain but not on the server, the format name returned is &lt;computer_name&gt;\&lt;user_name&gt; where &lt;computer_name&gt; is the name of the server that holds the account.

If the account is on the same server as the fax server, just the &lt;user_name&gt; of the account is returned.




## -see-also




<a href="https://msdn.microsoft.com/85adc440-3dc8-47ce-aae8-dfb04f824b09">FaxAccount</a>



<a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a>
 

 

