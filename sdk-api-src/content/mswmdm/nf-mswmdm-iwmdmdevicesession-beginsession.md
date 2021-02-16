---
UID: NF:mswmdm.IWMDMDeviceSession.BeginSession
title: IWMDMDeviceSession::BeginSession (mswmdm.h)
description: The BeginSession method begins a device session.
helpviewer_keywords: ["BeginSession","BeginSession method [windows Media Device Manager]","BeginSession method [windows Media Device Manager]","IWMDMDeviceSession interface","IWMDMDeviceSession interface [windows Media Device Manager]","BeginSession method","IWMDMDeviceSession.BeginSession","IWMDMDeviceSession::BeginSession","IWMDMDeviceSessionBeginSession","mswmdm/IWMDMDeviceSession::BeginSession","wmdm.iwmdmdevicesession_beginsession"]
old-location: wmdm\iwmdmdevicesession_beginsession.htm
tech.root: WMDM
ms.assetid: 7077e594-58ed-497d-893d-81eeb317b274
ms.date: 12/05/2018
ms.keywords: BeginSession, BeginSession method [windows Media Device Manager], BeginSession method [windows Media Device Manager],IWMDMDeviceSession interface, IWMDMDeviceSession interface [windows Media Device Manager],BeginSession method, IWMDMDeviceSession.BeginSession, IWMDMDeviceSession::BeginSession, IWMDMDeviceSessionBeginSession, mswmdm/IWMDMDeviceSession::BeginSession, wmdm.iwmdmdevicesession_beginsession
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMDeviceSession::BeginSession
 - mswmdm/IWMDMDeviceSession::BeginSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMDeviceSession.BeginSession
---

# IWMDMDeviceSession::BeginSession


## -description

The <b>BeginSession</b> method begins a device session.

## -parameters

### -param type [in]

A <a href="/windows/desktop/WMDM/wmdm-session-type">WMDM_SESSION_TYPE</a> describing the type of session to begin. This is a bitwise <b>OR</b> of any values except WMDM_SESSION_NONE. The same type (or combination of types) must be specified during <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicesession-endsession">EndSession</a>.

### -param pCtx [in]

Optional pointer to a caller-allocated session context buffer for private communication between the application and the service provider. Applications having knowledge of the underlying service provider can use this buffer to pass context-specific data to it. Windows Media Device Manager does not do anything with this context. The caller is responsible for freeing this buffer.

### -param dwSizeCtx [in]

Size of the context buffer, in bytes. If the size is 0, <i>pCtx</i> is ignored. If the size is non-zero, <i>pCtx</i> must be a valid pointer.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

Bundling several operations into a session does not cause all actions to be postponed and performed in a group; all actions (such as a call to <b>Insert</b>) will still be performed synchronously as called. Rather, using a session allows Windows Media Device Manager components (such as the secure content provider and service provider) to perform some of the operations only once per session, which provides performance improvements. For example, during file transfer to a device, the secure content provider can acquire the device certificate once at the beginning of the session instead of once for every file transfer.

Applications can call <b>BeginSession</b> on a Windows Media Device Manager device object before doing a set of operations and <b>EndSession</b> when they are done.

The application typically calls <b>BeginSession</b> during multiple file transfers or deletions. In response to that, Windows Media Device Manager calls <b>BeginSession</b> or <b>EndSession</b> on the secure content provider and the service provider. In response, the secure content provider and the service provider can perform once-per-session operations. If opening the session fails on any of these components, Windows Media Device Manager returns a failure returned by the component.

Sessions are implemented on a per-device basis. Sessions on different devices do not interfere with each other.

The following restrictions apply to sessions:

<ol>
<li>Only one session can be active at a time for a particular device. Attempting to open more than one session on a device will result in an error.</li>
<li>
Session types can be combined. The same set of flags must be specified during <b>BeginSession</b> and <b>EndSession</b>. Therefore, it is not possible to end only part of the session.

For example, if <b>BeginSession</b> is called with

WMDM_SESSION_TRANSFER_TO_DEVICE | WMDM_SESSION_DELETE

Then <b>EndSession</b> should also be called with

WMDM_SESSION_TRANSFER_TO_DEVICE | WMDM_SESSION_DELETE

Otherwise, Windows Media Device Manager will return E_INVALIDARG.

</li>
<li>Windows Media Device Manager sessions are simply a bracketing mechanism for optimizations and do not have any implications regarding locking or ownership of the device. Service provider or the lower level device driver will still need to synchronize device access that may result from different Windows Media Device Manager applications.</li>
</ol>

#### Examples

The following C++ code demonstrates using a session to bundle an <b>Insert3</b> call on a device. The code loops through a number of files stored in a vector and sends them to the device.


```cpp

// Get the session interface.
CComQIPtr<IWMDMDeviceSession> pSession(pDevice);
if (pDevice == NULL)
{
    // TODO: Display a message that the application couldn't get an 
    // IWMDMDeviceSession interface.
    return E_NOINTERFACE;
}

// Start the session. We don't use a custom buffer.
hr = pSession->BeginSession(WMDM_SESSION_TRANSFER_TO_DEVICE, NULL, NULL);
if (hr != S_OK)
{
    // TODO: Display a message indicating that the session failed to start.
    return hr;
}
else
{
    // TODO: Display a message that the session started.
}


// Insert files. These calls happen synchronously.
UINT flags = WMDM_MODE_BLOCK | WMDM_STORAGECONTROL_INSERTINTO | WMDM_FILE_CREATE_OVERWRITE | WMDM_CONTENT_FILE;
CComPtr<IWMDMStorage> pNewStorage;
for(int i = 0; i < sourceFiles.size(); i++)
{
    hr = pStorageControl3->Insert3(
        flags,
        WMDM_FILE_ATTR_FOLDER,
        sourceFiles[i],
        NULL, // Use default name.
        NULL, // Don't specify IWMDMOperation.
        NULL, // Don't specify IWMDMProgress.
        NULL, // Don't specify metadata.
        NULL, // Nothing to send to the SCP.
        &pNewStorage);

    if (pNewStorage != NULL)
        pNewStorage.Release();
    CHECK_HR(hr, "Sent file " << sourceFiles[i] << " to the device.", "Couldn't send file " << sourceFiles[i] << " to the device");
}

// Close the session.
hr = pSession->EndSession(WMDM_SESSION_TRANSFER_TO_DEVICE, NULL, NULL);
CHECK_HR(hr,"Closed the session.","Couldn't close the session.");

```

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession">IWMDMDeviceSession Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicesession-endsession">IWMDMDeviceSession::EndSession</a>



<a href="/windows/desktop/WMDM/wmdm-session-type">WMDM_SESSION_TYPE</a>