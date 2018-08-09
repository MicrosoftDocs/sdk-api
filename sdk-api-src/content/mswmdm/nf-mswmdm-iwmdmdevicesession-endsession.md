---
UID: NF:mswmdm.IWMDMDeviceSession.EndSession
title: IWMDMDeviceSession::EndSession
author: windows-sdk-content
description: The EndSession method ends a device session.
old-location: wmdm\iwmdmdevicesession_endsession.htm
old-project: WMDM
ms.assetid: f587a20a-936f-49a4-8e56-2e05b3d295f6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: EndSession, EndSession method [windows Media Device Manager], EndSession method [windows Media Device Manager],IWMDMDeviceSession interface, IWMDMDeviceSession interface [windows Media Device Manager],EndSession method, IWMDMDeviceSession.EndSession, IWMDMDeviceSession::EndSession, IWMDMDeviceSessionEndSession, mswmdm/IWMDMDeviceSession::EndSession, wmdm.iwmdmdevicesession_endsession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MSVidCtlStateList
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
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMDeviceSession::EndSession


## -description



The <b>EndSession</b> method ends a device session.




## -parameters




### -param type [in]

A <a href="https://msdn.microsoft.com/e4ed41c0-521f-4da0-8361-287b64d74d77">WMDM_SESSION_TYPE</a> describing the type of session to end. This must be the same bitwise <b>OR</b> of the values specified in <a href="https://msdn.microsoft.com/7077e594-58ed-497d-893d-81eeb317b274">BeginSession</a>.


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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



A session brackets a group of operations to a device, allowing Windows Media Device Manager components to optimize performance by performing common setup and shutdown functions only once, rather than with each individual transfer. For details see <b>BeginSession</b>.

In response to an <b>EndSession</b> call, Windows Media Device Manager calls <b>EndSession</b> on the secure content provider and the service provider. If either of them fails the call, Windows Media Device Manager returns an error. In that case, it is possible that <b>EndSession</b> succeeded for one of the components.


#### Examples

The following C++ code demonstrates using a session to bundle an <b>Insert3</b> call on a device. The code loops through a number of files stored in a vector and sends them to the device.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Get the session interface.
CComQIPtr&lt;IWMDMDeviceSession&gt; pSession(pDevice);
if (pDevice == NULL)
{
    // TODO: Display a message that the app wasn't able to retrieve the IWMDMDeviceSession interface.
    return E_NOINTERFACE;
}

// Start the session. We don't use a custom buffer.
hr = pSession-&gt;BeginSession(WMDM_SESSION_TRANSFER_TO_DEVICE, NULL, NULL);
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
CComPtr&lt;IWMDMStorage&gt; pNewStorage;
for(int i = 0; i &lt; sourceFiles.size(); i++)
{
    hr = pStorageControl3-&gt;Insert3(
        flags,
        WMDM_FILE_ATTR_FOLDER,
        sourceFiles[i],
        NULL, // Use default name.
        NULL, // Don't specify IWMDMOperation
        NULL, // Don't specify IWMDMProgress
        NULL, // Don't specify metadata
        NULL, // Nothing to send to the SCP.
        &amp;pNewStorage);

    if (pNewStorage != NULL)
        pNewStorage.Release();
    CHECK_HR(hr, "Sent file " &lt;&lt; sourceFiles[i] &lt;&lt; " to the device.", "Couldn't send file " &lt;&lt; sourceFiles[i] &lt;&lt; " to the device");
}

// Close the session.
hr = pSession-&gt;EndSession(WMDM_SESSION_TRANSFER_TO_DEVICE, NULL, NULL);
CHECK_HR(hr,"Closed the session.","Couldn't close the session.");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/37a57fbe-d0f8-44ee-b6c5-2c6a34e12f2b">IWMDMDeviceSession Interface</a>



<a href="https://msdn.microsoft.com/7077e594-58ed-497d-893d-81eeb317b274">IWMDMDeviceSession::BeginSession</a>



<a href="https://msdn.microsoft.com/e4ed41c0-521f-4da0-8361-287b64d74d77">WMDM_SESSION_TYPE</a>
 

 

