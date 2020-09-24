---
UID: NF:wincrypt.CertControlStore
title: CertControlStore function (wincrypt.h)
description: Allows an application to be notified when there is a difference between the contents of a cached store in use and the contents of that store as it is persisted to storage.
helpviewer_keywords: ["CERT_STORE_CTRL_AUTO_RESYNC","CERT_STORE_CTRL_CANCEL_NOTIFY","CERT_STORE_CTRL_COMMIT","CERT_STORE_CTRL_COMMIT_CLEAR_FLAG","CERT_STORE_CTRL_COMMIT_FORCE_FLAG","CERT_STORE_CTRL_INHIBIT_DUPLICATE_HANDLE_FLAG","CERT_STORE_CTRL_NOTIFY_CHANGE","CERT_STORE_CTRL_RESYNC","CertControlStore","CertControlStore function [Security]","_crypto2_certcontrolstore","security.certcontrolstore","wincrypt/CertControlStore"]
old-location: security\certcontrolstore.htm
tech.root: security
ms.assetid: 04cd9349-50c1-44b4-b080-631a24a80d70
ms.date: 12/05/2018
ms.keywords: CERT_STORE_CTRL_AUTO_RESYNC, CERT_STORE_CTRL_CANCEL_NOTIFY, CERT_STORE_CTRL_COMMIT, CERT_STORE_CTRL_COMMIT_CLEAR_FLAG, CERT_STORE_CTRL_COMMIT_FORCE_FLAG, CERT_STORE_CTRL_INHIBIT_DUPLICATE_HANDLE_FLAG, CERT_STORE_CTRL_NOTIFY_CHANGE, CERT_STORE_CTRL_RESYNC, CertControlStore, CertControlStore function [Security], _crypto2_certcontrolstore, security.certcontrolstore, wincrypt/CertControlStore
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertControlStore
 - wincrypt/CertControlStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertControlStore
---

# CertControlStore function


## -description

The <b>CertControlStore</b> function allows an application to be notified when there is a difference between the contents of a cached store in use and the contents of that store as it is persisted to storage. Differences can occur as another <a href="/windows/desktop/SecGloss/p-gly">process</a> makes a change that affects the store as it is persisted.

The <b>CertControlStore</b> function can be used to synchronize a cached store, if necessary, and provides a means to commit changes made in the cached store to persisted storage.

## -parameters

### -param hCertStore [in]

Handle of the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param dwFlags [in]

If the <i>dwCtrlType</i> parameter is set to CERT_STORE_CTRL_COMMIT, this parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTRL_COMMIT_FORCE_FLAG"></a><a id="cert_store_ctrl_commit_force_flag"></a><dl>
<dt><b>CERT_STORE_CTRL_COMMIT_FORCE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Forces the contents of the cache memory store to be copied to permanent storage even if the cache has not been changed.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTRL_COMMIT_CLEAR_FLAG"></a><a id="cert_store_ctrl_commit_clear_flag"></a><dl>
<dt><b>CERT_STORE_CTRL_COMMIT_CLEAR_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Inhibits the copying of the contents of the cache memory store to permanent storage even when the store is closed.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTRL_INHIBIT_DUPLICATE_HANDLE_FLAG"></a><a id="cert_store_ctrl_inhibit_duplicate_handle_flag"></a><dl>
<dt><b>CERT_STORE_CTRL_INHIBIT_DUPLICATE_HANDLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Inhibits a duplicate handle of the event HANDLE. If this flag is set, <b>CertControlStore</b> with CERT_STORE_CTRL_CANCEL_NOTIFY passed must be called for this event HANDLE before closing the <i>hCertStore</i> handle.

</td>
</tr>
</table>
 

If <i>dwCtrlType</i> is set to CERT_STORE_CTRL_NOTIFY_CHANGE or CERT_STORE_CTRL_RESYNC, the <i>dwFlags</i> parameter is not used and must be set to zero.

### -param dwCtrlType [in]

Control action to be taken by <b>CertControlStore</b>. The interpretations of <i>pvCtrlPara</i> and <i>dwFlags</i> depend on the value of <i>dwCtrlType</i>. Currently, the following  actions are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTRL_RESYNC"></a><a id="cert_store_ctrl_resync"></a><dl>
<dt><b>CERT_STORE_CTRL_RESYNC</b></dt>
</dl>
</td>
<td width="60%">
The cached store is resynchronized and made to match the persisted store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTRL_NOTIFY_CHANGE"></a><a id="cert_store_ctrl_notify_change"></a><dl>
<dt><b>CERT_STORE_CTRL_NOTIFY_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
A signal is returned in the space pointed to by <i>pvCtrlPara</i> to indicate that the current contents of the cached store differ from the store's persisted <a href="/windows/desktop/SecGloss/s-gly">state</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTRL_COMMIT"></a><a id="cert_store_ctrl_commit"></a><dl>
<dt><b>CERT_STORE_CTRL_COMMIT</b></dt>
</dl>
</td>
<td width="60%">
Any changes made to the cached store are copied to persisted storage. If no changes were made since the cached store was opened or since the last commit, the call is ignored. The call is also ignored if the store provider is a provider that automatically persists changes immediately.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTRL_AUTO_RESYNC"></a><a id="cert_store_ctrl_auto_resync"></a><dl>
<dt><b>CERT_STORE_CTRL_AUTO_RESYNC</b></dt>
</dl>
</td>
<td width="60%">
At the start of every enumeration or find store call, a check is made to determine whether a change has been made in the store. If the store has changed, a re-synchronization is done. This check is only done on first enumeration or find calls, when the <i>pPrevContext</i> is <b>NULL</b>.


The <b>pvCtrPara</b> member is not used and must be set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTRL_CANCEL_NOTIFY"></a><a id="cert_store_ctrl_cancel_notify"></a><dl>
<dt><b>CERT_STORE_CTRL_CANCEL_NOTIFY</b></dt>
</dl>
</td>
<td width="60%">
Cancels notification signaling of the event HANDLE passed in a previous CERT_STORE_CTRL_NOTIFY_CHANGE or CERT_STORE_CTRL_RESYNC. The <i>pvCtrlPara</i> parameter points to the event HANDLE to be canceled.

</td>
</tr>
</table>

### -param pvCtrlPara [in]

If <i>dwCtrlType</i> is CERT_STORE_NOTIFY_CHANGE, <i>pvCtrlPara</i> is set to the address of a handle where the system signals the notification change event when a change from the persisted <a href="/windows/desktop/SecGloss/s-gly">state</a> of the store is detected. The handle must be initialized with a call to the function <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>. The <i>pvCtrlPara</i> parameter can be set to <b>NULL</b> for registry-based stores. If <i>pvCtrlPara</i> is <b>NULL</b>, an internal notification change event is created and registered to be signaled. Using the internal notification change event allows resynchronization operations only if the store was changed. 




If <i>dwCtrlType</i> is CERT_STORE_CTRL_RESYNC, set <i>pvCtrlPara</i> to the address of the event handle to be signaled on the next change in the persisted store. Typically, this address is the address of the event handle passed with CERT_STORE_CTRL_NOTIFY_CHANGE during initialization. The event handle passed is rearmed. If <i>pvCtrlPara</i> is set to <b>NULL</b>, no event is rearmed.

If <i>dwCtrlType</i> CERT_STORE_CTRL_COMMIT, <i>pvCtrlPara</i> is not used and must be set to <b>NULL</b>.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If <i>dwCtrlType</i> is CERT_STORE_NOTIFY_CHANGE, the function returns nonzero if a handle for the event signal was successfully set up. The function returns zero if the event handle was not set up.

If <i>dwCtrlType</i> is CERT_STORE_CTRL_RESYNC, the function returns nonzero if the resynchronization succeeded. The function returns zero if the resynchronization failed.

If <i>dwCtrlType</i> is CERT_STORE_CTRL_COMMIT, the function returns nonzero to indicate the successful completion of the commit to persisted storage. The function returns zero if the commit failed.

Some providers might not support specific control types. In these cases, <b>CertControlStore</b> returns zero and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> is set to the ERROR_NOT_SUPPORTED code.

## -remarks

Resynchronization of a store can be done at any time. It need not follow a signaled notification change event.

CERT_STORE_CTRL_NOTIFY_CHANGE is supported on registry-based store providers by using the <a href="/windows/desktop/api/winreg/nf-winreg-regnotifychangekeyvalue">RegNotifyChangeKeyValue</a> function.

<b>CertControlStore</b> using CERT_STORE_CTRL_NOTIFY_CHANGE is called once for each event handle to be passed with CERT_STORE_CTRL_RESYNC. These calls using CERT_STORE_CTRL_NOTIFY_CHANGE must be made after each event is created and not after an event has been signaled.


#### Examples

The following example shows allowing an application to be notified when there is a difference between the contents of a cached store in use and the contents of that store as it is persisted to storage. For the full example including the complete context for this example, see 
<a href="/windows/desktop/SecCrypto/example-c-program-setting-and-getting-certificate-store-properties">Example C Program: Setting and Getting Certificate Store Properties</a>.


```cpp

//--------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE hCertStore;     // Original certificate store
HANDLE     hEvent;
BOOL       fSignal;

//--------------------------------------------------------------------
// Initialize an event.

if(hEvent = CreateEvent(
    NULL,
    FALSE,          // Manual reset is FALSE
    FALSE,          // The initial state of the event is FALSE
    NULL))
{
     printf("An event has been created. \n");
}
else
{
     printf("The event was not created. \n");
     exit(1);
}

//--------------------------------------------------------------------
// Open the MY certificate store. 

if ( hCertStore = CertOpenStore(
    CERT_STORE_PROV_SYSTEM,
    0,
    NULL,
    CERT_SYSTEM_STORE_CURRENT_USER,
    L"MY"))
{
    printf("The MY store is open. \n");
}
else
{
    printf("The MY store did not open. \n");
    exit(1);
}

//--------------------------------------------------------------------
//  Call CertControlStore the first time with 
//  CERT_CONTROL_STORE_NOTIFY_CHANGE.

if(CertControlStore(
    hCertStore,                        //  The store to be controlled
    0,                                 //  Not used 
    CERT_STORE_CTRL_NOTIFY_CHANGE,     //  Control action type
    &hEvent))                          //  Points to the event handle
                           //  When a change is detected,
                           //  a signal is written to the 
                    //  memory location pointed to by
                    //  hHandle.
{
    printf("Notify change worked. \n");
}
else
{
    printf("Notify change failed. \n");
    exit(1);
}

//--------------------------------------------------------------------
// Wait for the store to change.

fSignal = (WAIT_OBJECT_0 == WaitForSingleObjectEx(
    hEvent,
    1000,        // Number of milliseconds to wait;
            // Use INFINITE to wait indefinitely for
            // a change
    FALSE));

if (fSignal)
{

//--------------------------------------------------------------------
// The store has changed.
// Call the function a second time with CERT_STORE_CTRL_RESYNC.

    if(CertControlStore(
        hCertStore,             // The store to be controlled
        0,                      // Not used
        CERT_STORE_CTRL_RESYNC, // Control action type
        &hEvent))               // The handle of the event 
                                // to be rearmed

    printf("Resynchronization worked. \n");
    
    else
    {
        printf("Resynchronization failed. \n");
        exit(1);
    }
}
else
{
      printf("The store was not changed. \n");
      printf("Resynchronization was not needed. \n");
}

// Release the handle to the store.

if(CertCloseStore(hCertStore,
                   0))
{
        printf("The MY store was closed. \n");
}
else
{
        printf("An error occurred. The MY store was not closed. \n");
}

```

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Store Functions</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>