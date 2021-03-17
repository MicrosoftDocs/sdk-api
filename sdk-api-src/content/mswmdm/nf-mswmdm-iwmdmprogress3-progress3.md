---
UID: NF:mswmdm.IWMDMProgress3.Progress3
title: IWMDMProgress3::Progress3 (mswmdm.h)
description: The Progress3 method is called by Windows Media Device Manager to indicate the status of an action in progress.
helpviewer_keywords: ["IWMDMProgress3 interface [windows Media Device Manager]","Progress3 method","IWMDMProgress3.Progress3","IWMDMProgress3::Progress3","IWMDMProgress3Progress3","Progress3","Progress3 method [windows Media Device Manager]","Progress3 method [windows Media Device Manager]","IWMDMProgress3 interface","mswmdm/IWMDMProgress3::Progress3","wmdm.iwmdmprogress3_progress3"]
old-location: wmdm\iwmdmprogress3_progress3.htm
tech.root: WMDM
ms.assetid: 33f1de9c-f2eb-4b83-89a1-404a8c50ee08
ms.date: 12/05/2018
ms.keywords: IWMDMProgress3 interface [windows Media Device Manager],Progress3 method, IWMDMProgress3.Progress3, IWMDMProgress3::Progress3, IWMDMProgress3Progress3, Progress3, Progress3 method [windows Media Device Manager], Progress3 method [windows Media Device Manager],IWMDMProgress3 interface, mswmdm/IWMDMProgress3::Progress3, wmdm.iwmdmprogress3_progress3
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
 - IWMDMProgress3::Progress3
 - mswmdm/IWMDMProgress3::Progress3
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
 - IWMDMProgress3.Progress3
---

# IWMDMProgress3::Progress3


## -description

The <b>Progress3</b> method is called by Windows Media Device Manager to indicate the status of an action in progress. This method extends <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-progress">IWMDMProgress::Progress</a> by providing additional input parameters for the identification (ID) of the event and for a pointer to the context of the commands.

## -parameters

### -param EventId [in]

<b>GUID</b> specifying the event ID for which progress notifications are being sent. Possible values are shown in the following table.

<table>
<tr>
<th>Event
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>SCP_EVENTID_ACQSECURECLOCK</td>
<td>Windows Media Device Manager is acquiring a secure clock from server.</td>
</tr>
<tr>
<td>SCP_EVENTID_NEEDTOINDIV</td>
<td>The device is being individualized. This is not currently used.</td>
</tr>
<tr>
<td>SCP_EVENTID_DRMINFO</td>
<td>
This event ID is used to notify the application with the version DRM header found in the content for each file.

The OPAQUECOMMAND structure returned has the <i>guidCommand</i> parameter set to SCP_PARAMID_DRMVERSION.

In addition, the data specifies one of the following flags:

WMDM_SCP_DRMINFO_NOT_DRMPROTECTED

WMDM_SCP_DRMINFO_V1HEADER

WMDM_SCP_DRMINFO_V2HEADER

</td>
</tr>
<tr>
<td>EVENT_WMDM_CONTENT_TRANSFER</td>
<td>Content is being transferred to or from the device.</td>
</tr>
</table>

### -param dwTranspiredTicks [in]

<b>DWORD</b> specifying the number of ticks that have transpired so far.

### -param pContext [in, out]

Pointer to an <a href="/windows/desktop/WMDM/opaquecommand">OPAQUECOMMAND</a> structure containing a command sent directly to the device without being handled by Windows Media Device Manager. This parameter is optional and can be <b>NULL</b>. If the event is SCP_EVENTID_DRMINFO, the data in this parameter will have the SCP_PARAMID_DRMVERSION GUID.

## -returns

The application should return one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Device Manager should cancel the current operation without waiting for it to finish. If the application is using block mode, then Windows Media Device Manager will return this error to the application.

</td>
</tr>
</table>

## -remarks

The interface that owns the method that is implementing an operation calls the <b>Progress3</b> method as the operation defined by the method is carried out. The intention is that <b>Progress3</b> will be called once per estimated tick. However, the <i>dwTranspiredTicks</i> parameter must be checked on each call because the operation being performed may not guarantee one call for each estimated tick.

The application returns S_OK to the calling method to indicate that the operation should continue. The application returns WMDM_E_USER_CANCELLED to indicate that the operation should be canceled. If the application is using block mode and returns WMDM_E_USER_CANCELLED, then Windows Media Device Manager will return this same error to the application.


#### Examples

The following C++ code shows an example implementation of <b>Progress3</b>.


```cpp

HRESULT Progress3(GUID  EventId, DWORD  dwTranspiredTicks, OPAQUECOMMAND*  pContext)
{
    WCHAR strGuid[64];
    ZeroMemory(strGuid, 64);
    StringFromGUID2(reinterpret_cast<GUID&>(EventId),(LPOLESTR)strGuid, 64);
    // TODO: Display the message: "Progress3 called. GUID value: " 
    // followed by the strGUID value.
    // TODO: Display the message: "Progress3 dwTranspiredTicks: " 
    // followed by the dwTranspiredTicks value.

    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-progress">IWMDMProgress::Progress</a>