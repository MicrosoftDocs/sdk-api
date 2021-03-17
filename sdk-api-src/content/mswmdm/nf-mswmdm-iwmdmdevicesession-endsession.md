---
UID: NF:mswmdm.IWMDMDeviceSession.EndSession
title: IWMDMDeviceSession::EndSession (mswmdm.h)
description: The EndSession method ends a device session.
helpviewer_keywords: ["EndSession","EndSession method [windows Media Device Manager]","EndSession method [windows Media Device Manager]","IWMDMDeviceSession interface","IWMDMDeviceSession interface [windows Media Device Manager]","EndSession method","IWMDMDeviceSession.EndSession","IWMDMDeviceSession::EndSession","IWMDMDeviceSessionEndSession","mswmdm/IWMDMDeviceSession::EndSession","wmdm.iwmdmdevicesession_endsession"]
old-location: wmdm\iwmdmdevicesession_endsession.htm
tech.root: WMDM
ms.assetid: f587a20a-936f-49a4-8e56-2e05b3d295f6
ms.date: 12/05/2018
ms.keywords: EndSession, EndSession method [windows Media Device Manager], EndSession method [windows Media Device Manager],IWMDMDeviceSession interface, IWMDMDeviceSession interface [windows Media Device Manager],EndSession method, IWMDMDeviceSession.EndSession, IWMDMDeviceSession::EndSession, IWMDMDeviceSessionEndSession, mswmdm/IWMDMDeviceSession::EndSession, wmdm.iwmdmdevicesession_endsession
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
 - IWMDMDeviceSession::EndSession
 - mswmdm/IWMDMDeviceSession::EndSession
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
 - IWMDMDeviceSession.EndSession
---

# IWMDMDeviceSession::EndSession


## -description

The <b>EndSession</b> method ends a device session.

## -parameters

### -param type [in]

A <a href="/windows/desktop/WMDM/wmdm-session-type">WMDM_SESSION_TYPE</a> describing the type of session to end. This must be the same bitwise <b>OR</b> of the values specified in <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicesession-beginsession">BeginSession</a>.

### -param pCtx [in]

Optional pointer to a caller-allocated session context buffer for private communication between the application and the service provider. Applications having knowledge of the underlying service provider can use this buffer to pass context-specific data to it. Windows Media Device Manager does not do anything with this context. The caller is responsible for freeing this buffer.

### -param dwSizeCtx [in]

Size of the context buffer, in bytes. If the size is 0, <i>pCtx</i> is ignored. If the size is non-zero, <i>pCtx</i> must be a valid pointer

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

A session brackets a group of operations to a device, allowing Windows Media Device Manager components to optimize performance by performing common setup and shutdown functions only once, rather than with each individual transfer. For details see <b>BeginSession</b>.

In response to an <b>EndSession</b> call, Windows Media Device Manager calls <b>EndSession</b> on the secure content provider and the service provider. If either of them fails the call, Windows Media Device Manager returns an error. In that case, it is possible that <b>EndSession</b> succeeded for one of the components.


#### Examples

The following C++ code demonstrates using a session to bundle an <b>Insert3</b> call on a device. The code loops through a number of files stored in a vector and sends them to the device.


```cpp

// Get the session interface.
CComQIPtr<IWMDMDeviceSession> pSession(pDevice);
if (pDevice == NULL)
{
    // TODO: Display a message that the app wasn't able to retrieve the IWMDMDeviceSession interface.
    return E_NOINTERFACE;
}

// Start the session. We don't use a custom buffer.
hr = pSession->BeginSession(WMDM_SESSION_TRANSFER_TO_DEVICE, NULL, NULL);
if (hr != S_OK)
{
    / /TODO: Display a message indicating that the session failed to start.
    return hr;
}
else
{
    // TODO: Display a message indicating that the session started.
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
        NULL, // Don't specify IWMDMOperation
        NULL, // Don't specify IWMDMProgress
        NULL, // Don't specify metadata
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



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicesession-beginsession">IWMDMDeviceSession::BeginSession</a>



<a href="/windows/desktop/WMDM/wmdm-session-type">WMDM_SESSION_TYPE</a>