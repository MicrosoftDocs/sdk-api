---
UID: NF:faxcomex.IFaxAccountSet.AddAccount
title: IFaxAccountSet::AddAccount
author: windows-sdk-content
description: Adds a fax account to the fax server and returns the new IFaxAccount object.
old-location: fax\_mfax_faxaccountset_addaccount_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountset\addaccount.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: AddAccount, AddAccount method [Fax Service], AddAccount method [Fax Service],FaxAccountSet object, FaxAccountSet object [Fax Service],AddAccount method, FaxAccountSet.AddAccount, IFaxAccountSet.AddAccount, IFaxAccountSet::AddAccount, _mfax_faxaccountset.addaccount, fax._mfax_faxaccountset_addaccount, fax._mfax_faxaccountset_addaccount_vb
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
 - FaxAccountSet.AddAccount
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxAccountSet::AddAccount


## -description


Adds a fax account to the fax server and returns the new <a href="https://msdn.microsoft.com/en-us/library/Aa359058(v=VS.85).aspx">IFaxAccount</a> object.


## -parameters




### -param bstrAccountName [in]

Type: <b>String</b>

Specifies a null-terminated string that contains a name for the new account.


### -param pFaxAccount






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa359058(v=VS.85).aspx">IFaxAccount</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa359058(v=VS.85).aspx">IFaxAccount</a> object.




## -remarks



<i>bstrAccountName</i> must be of the form &lt;domainName&gt;\&lt;username&gt; or just &lt;username&gt; for local users.

When the new account is returned, all its values except the name are set to defaults.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358935(v=VS.85).aspx">FaxAccountSet</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa359014(v=VS.85).aspx">IFaxAccountSet</a>
 

 

