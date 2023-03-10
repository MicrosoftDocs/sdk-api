---
UID: NF:certexit.ICertExit.Initialize
title: ICertExit::Initialize (certexit.h)
description: Called by the server engine when it initializes itself.
helpviewer_keywords: ["CCertExit object [Security]","Initialize method","EXITEVENT_CERTDENIED","EXITEVENT_CERTISSUED","EXITEVENT_CERTPENDING","EXITEVENT_CERTRETRIEVEPENDING","EXITEVENT_CERTREVOKED","EXITEVENT_CRLISSUED","EXITEVENT_SHUTDOWN","ICertExit interface [Security]","Initialize method","ICertExit.Initialize","ICertExit2 interface [Security]","Initialize method","ICertExit2::Initialize","ICertExit::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","CCertExit object","Initialize method [Security]","ICertExit interface","Initialize method [Security]","ICertExit2 interface","_certsrv_icertexit_initialize","certexit/ICertExit2::Initialize","certexit/ICertExit::Initialize","security.icertexit2_initialize"]
old-location: security\icertexit2_initialize.htm
tech.root: security
ms.assetid: 61d27de8-f940-4f18-ba44-7e91378f035c
ms.date: 12/05/2018
ms.keywords: CCertExit object [Security],Initialize method, EXITEVENT_CERTDENIED, EXITEVENT_CERTISSUED, EXITEVENT_CERTPENDING, EXITEVENT_CERTRETRIEVEPENDING, EXITEVENT_CERTREVOKED, EXITEVENT_CRLISSUED, EXITEVENT_SHUTDOWN, ICertExit interface [Security],Initialize method, ICertExit.Initialize, ICertExit2 interface [Security],Initialize method, ICertExit2::Initialize, ICertExit::Initialize, Initialize, Initialize method [Security], Initialize method [Security],CCertExit object, Initialize method [Security],ICertExit interface, Initialize method [Security],ICertExit2 interface, _certsrv_icertexit_initialize, certexit/ICertExit2::Initialize, certexit/ICertExit::Initialize, security.icertexit2_initialize
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
 - ICertExit::Initialize
 - certexit/ICertExit::Initialize
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
 - ICertExit2.Initialize
 - ICertExit.Initialize
 - CCertExit.Initialize
---

# ICertExit::Initialize


## -description

The <b>Initialize</b> method is called by the server engine when it initializes itself.

 The call to the exit module's <b>Initialize</b> method allows the exit module to perform initialization and inform the server engine which kinds of events it would like to be notified of.

## -parameters

### -param strConfig [in]

Represents the name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig2">ICertConfig2</a>.

### -param pEventMask [out, retval]

A pointer to the value that represents the events for which the exit module requests notification. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<td width="40%"><a id="EXITEVENT_CERTRETRIEVEPENDING"></a><a id="exitevent_certretrievepending"></a><dl>
<dt><b>EXITEVENT_CERTRETRIEVEPENDING</b></dt>
</dl>
</td>
<td width="60%">
Successful call to 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">RetrievePending</a>.

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
<td width="40%"><a id="EXITEVENT_CRLISSUED"></a><a id="exitevent_crlissued"></a><dl>
<dt><b>EXITEVENT_CRLISSUED</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/c-gly">Certificate revocation list</a> issued.

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

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and *<i>pEventMask</i> is set to a combination of the flags in the table below (or EXITEVENT_INVALID if the exit module does not want to be notified of any events).

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

If the exit module does not want to be notified of any events, then the flag EXITEVENT_INVALID should be set.

<h3>VB</h3>
 The return value is a mask that contains flags that indicate the events for which the exit module requests notification. After the call, all events of those types will be signaled by the server engine to the exit module through a call to 
<a href="/windows/desktop/api/certexit/nf-certexit-icertexit-notify">Notify</a>. Any or all of the following flags may be set.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXITEVENT_CERTDENIED</b></dt>
<dt>&amp;H4</dt>
</dl>
</td>
<td width="60%">
Certificate denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXITEVENT_CERTISSUED</b></dt>
<dt>&amp;H1</dt>
</dl>
</td>
<td width="60%">
Certificate issued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXITEVENT_CERTPENDING</b></dt>
<dt>&amp;H2</dt>
</dl>
</td>
<td width="60%">
Certificate pending.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXITEVENT_CERTRETRIEVEPENDING</b></dt>
<dt>&amp;H10</dt>
</dl>
</td>
<td width="60%">
Successful call to 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">RetrievePending</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXITEVENT_CERTREVOKED</b></dt>
<dt>&amp;H8</dt>
</dl>
</td>
<td width="60%">
Certificate revoked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXITEVENT_CRLISSUED</b></dt>
<dt>&amp;H20</dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/c-gly">Certificate revocation list</a> issued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXITEVENT_INVALID</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The event is currently not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EXITEVENT_SHUTDOWN</b></dt>
<dt>&amp;H40</dt>
</dl>
</td>
<td width="60%">
Certificate Services shutdown.

</td>
</tr>
</table>

## -remarks

When you write a custom exit module, implement this method.


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certexit.h>

STDMETHODIMP CCertExit::Initialize(
    /* [in] */ BSTR const strConfig,
    /* [retval][out] */ LONG __RPC_FAR *pEventMask)
{
    // Verify valid pointer passed in.
    if (NULL == pEventMask)
        return ( E_POINTER );  // Bad pointer

    // strConfig can be used by the Exit module.
    // Here, it is stored in a BSTR member variable.
    // Remember to call SysFreeString to free m_strConfig when done.
    m_strConfig = SysAllocString( strConfig );
    // Check to determine whether there was enough memory.
    if (NULL == m_strConfig)
        return ( E_OUTOFMEMORY );  // Not enough memory

    // Inform server engine (CA) that we're interested in
    // the following events.
    *pEventMask = EXITEVENT_CERTISSUED |
                  EXITEVENT_CERTPENDING |
                  EXITEVENT_CERTDENIED |
                  EXITEVENT_CERTREVOKED |
                  EXITEVENT_CERTRETRIEVEPENDING |
                  EXITEVENT_CRLISSUED |
                  EXITEVENT_SHUTDOWN;

    if ( fDebug )
    {
        printf("Exit's Initialize member called\n");
        printf("\tstrConfig = %ws\n", strConfig );
    }

    return( S_OK );
}
```

## -see-also

<a href="/windows/desktop/api/certexit/nn-certexit-icertexit">ICertExit</a>



<a href="/windows/desktop/api/certexit/nn-certexit-icertexit2">ICertExit2</a>



<a href="/windows/desktop/api/certexit/nf-certexit-icertexit-notify">Notify</a>