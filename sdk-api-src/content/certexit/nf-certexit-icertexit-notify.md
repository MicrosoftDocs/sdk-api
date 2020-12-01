---
UID: NF:certexit.ICertExit.Notify
title: ICertExit::Notify (certexit.h)
description: Called by the server engine to notify an exit module that an event has occurred.
helpviewer_keywords: ["CCertExit object [Security]","Notify method","EXITEVENT_CERTDENIED","EXITEVENT_CERTISSUED","EXITEVENT_CERTPENDING","EXITEVENT_CERTRETRIEVEPENDING","EXITEVENT_CERTREVOKED","EXITEVENT_CRLISSUED","EXITEVENT_SHUTDOWN","ICertExit interface [Security]","Notify method","ICertExit.Notify","ICertExit2 interface [Security]","Notify method","ICertExit2::Notify","ICertExit::Notify","Notify","Notify method [Security]","Notify method [Security]","CCertExit object","Notify method [Security]","ICertExit interface","Notify method [Security]","ICertExit2 interface","_certsrv_icertexit_notify","certexit/ICertExit2::Notify","certexit/ICertExit::Notify","security.icertexit2_notify"]
old-location: security\icertexit2_notify.htm
tech.root: security
ms.assetid: ebe4ef0c-5778-4a62-b112-9b16b250814f
ms.date: 12/05/2018
ms.keywords: CCertExit object [Security],Notify method, EXITEVENT_CERTDENIED, EXITEVENT_CERTISSUED, EXITEVENT_CERTPENDING, EXITEVENT_CERTRETRIEVEPENDING, EXITEVENT_CERTREVOKED, EXITEVENT_CRLISSUED, EXITEVENT_SHUTDOWN, ICertExit interface [Security],Notify method, ICertExit.Notify, ICertExit2 interface [Security],Notify method, ICertExit2::Notify, ICertExit::Notify, Notify, Notify method [Security], Notify method [Security],CCertExit object, Notify method [Security],ICertExit interface, Notify method [Security],ICertExit2 interface, _certsrv_icertexit_notify, certexit/ICertExit2::Notify, certexit/ICertExit::Notify, security.icertexit2_notify
req.header: certexit.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertExit::Notify
 - certexit/ICertExit::Notify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certexit.h
api_name:
 - ICertExit2.Notify
 - ICertExit.Notify
 - CCertExit.Notify
---

# ICertExit::Notify


## -description

The <b>Notify</b> method is called by the server engine to notify an exit module that an event has occurred.

## -parameters

### -param ExitEvent [in]

A mask that indicates the kind of exit event that has occurred. The mask can have one of the following flag-bits set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EXITEVENT_CERTISSUED"></a><a id="exitevent_certissued"></a><dl>
<dt><b>EXITEVENT_CERTISSUED</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued.

</td>
</tr>
<tr>
<td width="40%"><a id="EXITEVENT_CERTPENDING"></a><a id="exitevent_certpending"></a><dl>
<dt><b>EXITEVENT_CERTPENDING</b></dt>
</dl>
</td>
<td width="60%">
Certificate pending.

</td>
</tr>
<tr>
<td width="40%"><a id="EXITEVENT_CERTDENIED"></a><a id="exitevent_certdenied"></a><dl>
<dt><b>EXITEVENT_CERTDENIED</b></dt>
</dl>
</td>
<td width="60%">
Certificate denied.

</td>
</tr>
<tr>
<td width="40%"><a id="EXITEVENT_CERTREVOKED"></a><a id="exitevent_certrevoked"></a><dl>
<dt><b>EXITEVENT_CERTREVOKED</b></dt>
</dl>
</td>
<td width="60%">
Certificate revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="EXITEVENT_CERTRETRIEVEPENDING"></a><a id="exitevent_certretrievepending"></a><dl>
<dt><b>EXITEVENT_CERTRETRIEVEPENDING</b></dt>
</dl>
</td>
<td width="60%">
Successful call to 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">ICertRequest::RetrievePending</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="EXITEVENT_CRLISSUED"></a><a id="exitevent_crlissued"></a><dl>
<dt><b>EXITEVENT_CRLISSUED</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/c-gly">Certificate revocation list</a> (CRL) issued.

</td>
</tr>
<tr>
<td width="40%"><a id="EXITEVENT_SHUTDOWN"></a><a id="exitevent_shutdown"></a><dl>
<dt><b>EXITEVENT_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
Certificate Services shutdown.

</td>
</tr>
</table>

### -param Context [in]

Specifies a context handle that can be used to get properties associated with the event from the 
<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a> interface.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> is using multiple exit modules, Certificate Services will notify each exit module of the event (provided the exit module requested notification by means of 
<a href="/windows/desktop/api/certexit/nf-certexit-icertexit-initialize">Initialize</a>). The order in which the exit modules are notified should not be assumed, nor should one exit module depend on the processing of another exit module. Each notified exit module must return from 
<b>Notify</b> before the next exit module will be notified.


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certexit.h>

STDMETHODIMP CCertExit::Notify(
    /* [in] */ LONG ExitEvent,
    /* [in] */ LONG Context)
{
    char *pszEvent;
    HRESULT hr = S_OK;

    switch (ExitEvent)
    {
    case EXITEVENT_CERTISSUED:
        //  Call application-specific function for issued certs.
        hr = MyEventCertIssued(Context);
        pszEvent = "certissued";
        break;

    case EXITEVENT_CERTPENDING:
        pszEvent = "certpending";
        break;

    case EXITEVENT_CERTDENIED:
        pszEvent = "certdenied";
        break;

    case EXITEVENT_CERTREVOKED:
        pszEvent = "certrevoked";
        break;

    case EXITEVENT_CERTRETRIEVEPENDING:
        pszEvent = "retrievepending";
        break;

    case EXITEVENT_CRLISSUED:
        pszEvent = "crlissued";
        break;

    case EXITEVENT_SHUTDOWN:
        //  Call application-specific function for shutdown.
        hr = MyEventShutdown();
        pszEvent = "shutdown";
        break;

    default:
        pszEvent = "Unexpected event";
        break;
    }

    if ( fDebug )
    {
        //  Display what took place.
        printf("Exit::Notify(%s=%x, context=%u) return=%x\n",
                      pszEvent,
                      ExitEvent,
                      Context,
                      hr);
    }

    return(hr);
}
```

## -see-also

<a href="/windows/desktop/api/certexit/nn-certexit-icertexit">ICertExit</a>



<a href="/windows/desktop/api/certexit/nn-certexit-icertexit2">ICertExit2</a>