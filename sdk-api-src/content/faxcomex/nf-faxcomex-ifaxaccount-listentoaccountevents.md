---
UID: NF:faxcomex.IFaxAccount.ListenToAccountEvents
title: IFaxAccount::ListenToAccountEvents (faxcomex.h)
description: Sets the flags of a FAX_ACCOUNT_EVENTS_TYPE_ENUM variable that represents the events for which the account is listening.
helpviewer_keywords: ["IFaxAccount interface [Fax Service]","ListenToAccountEvents method","IFaxAccount.ListenToAccountEvents","IFaxAccount::ListenToAccountEvents","ListenToAccountEvents","ListenToAccountEvents method [Fax Service]","ListenToAccountEvents method [Fax Service]","IFaxAccount interface","_mfax_faxaccount.listentoaccountevents","fax._mfax_faxaccount_cpp_mfax_faxaccount_listentoaccountevents_cpp","fax._mfax_faxaccount_listentoaccountevents","faxcomex/IFaxAccount::ListenToAccountEvents"]
old-location: fax\_mfax_faxaccount_cpp_mfax_faxaccount_listentoaccountevents_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccount\listentoaccountevents.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccount interface [Fax Service],ListenToAccountEvents method, IFaxAccount.ListenToAccountEvents, IFaxAccount::ListenToAccountEvents, ListenToAccountEvents, ListenToAccountEvents method [Fax Service], ListenToAccountEvents method [Fax Service],IFaxAccount interface, _mfax_faxaccount.listentoaccountevents, fax._mfax_faxaccount_cpp_mfax_faxaccount_listentoaccountevents_cpp, fax._mfax_faxaccount_listentoaccountevents, faxcomex/IFaxAccount::ListenToAccountEvents
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxAccount::ListenToAccountEvents
 - faxcomex/IFaxAccount::ListenToAccountEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxAccount.ListenToAccountEvents
 - IFaxAccount.ListenToAccountEvents
---

# IFaxAccount::ListenToAccountEvents


## -description

Sets the flags of a <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_account_events_type_enum">FAX_ACCOUNT_EVENTS_TYPE_ENUM</a> variable that represents the events for which the account is listening.

## -parameters

### -param EventTypes [in]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_account_events_type_enum">FAX_ACCOUNT_EVENTS_TYPE_ENUM</a></b>

A variable that specifies the types of events for which the account is listening.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccount">FaxAccount</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>