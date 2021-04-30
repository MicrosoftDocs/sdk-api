---
UID: NF:mswmdm.IWMDMProgress3.Begin3
title: IWMDMProgress3::Begin3 (mswmdm.h)
description: The Begin3 method is called by Windows Media Device Manager to indicate that an operation is about to begin.
helpviewer_keywords: ["Begin3","Begin3 method [windows Media Device Manager]","Begin3 method [windows Media Device Manager]","IWMDMProgress3 interface","IWMDMProgress3 interface [windows Media Device Manager]","Begin3 method","IWMDMProgress3.Begin3","IWMDMProgress3::Begin3","IWMDMProgress3Begin3","mswmdm/IWMDMProgress3::Begin3","wmdm.iwmdmprogress3_begin3"]
old-location: wmdm\iwmdmprogress3_begin3.htm
tech.root: WMDM
ms.assetid: 8c794aff-9800-405e-853a-56dd5bd84665
ms.date: 12/05/2018
ms.keywords: Begin3, Begin3 method [windows Media Device Manager], Begin3 method [windows Media Device Manager],IWMDMProgress3 interface, IWMDMProgress3 interface [windows Media Device Manager],Begin3 method, IWMDMProgress3.Begin3, IWMDMProgress3::Begin3, IWMDMProgress3Begin3, mswmdm/IWMDMProgress3::Begin3, wmdm.iwmdmprogress3_begin3
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
 - IWMDMProgress3::Begin3
 - mswmdm/IWMDMProgress3::Begin3
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
 - IWMDMProgress3.Begin3
---

# IWMDMProgress3::Begin3


## -description

The <b>Begin3</b> method is called by Windows Media Device Manager to indicate that an operation is about to begin. An estimate of the duration of the operation is provided when possible. This method extends <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-begin">IWMDMProgress::Begin</a> by providing additional input parameters for the identification (ID) of the event and for a pointer to the optional context of the commands. The operation is identified by an event ID. The method allows the caller to pass an opaque data structure to the application.

## -parameters

### -param EventId [in]

A <b>GUID</b> identifying the operation that will begin. Possible values are shown in the following table.

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

The OPAQUECOMMAND structure returned has the <b>guidCommand</b> member set to SCP_PARAMID_DRMVERSION.

In addition, the OPAQUECOMMAND specifies one of the following flags:

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

### -param dwEstimatedTicks [in]

<b>DWORD</b> specifying the estimated number of ticks that are needed for the operation to complete. The number of ticks passed in <i>dwEstimatedTicks</i> is an estimate of how many ticks are needed for the operation to complete. During the course of the operation, the <b>Progress3</b> method is called to indicate how many ticks have transpired. Applications can use the estimate to configure display mechanisms that show progress.

### -param pContext [in, out]

Pointer to an <a href="/windows/desktop/WMDM/opaquecommand">OPAQUECOMMAND</a> structure containing a command sent to the device without being handled by Windows Media Device Manager. This parameter is optional and can be <b>NULL</b>.

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

The application returns S_OK to indicate that an operation should be continued and WMDM_E_USER_CANCELLED to indicate that the operation should be cancelled. If the application is using block mode and returns WMDM_E_USER_CANCELLED, then Windows Media Device Manager will return this same error to the application.


#### Examples

The following C++ code shows an example implementation of <b>Begin3</b>.


```cpp

HRESULT Begin3(GUID  EventId, DWORD  dwEstimatedTicks, OPAQUECOMMAND*  pContext)
{
    WCHAR strGuid[64];
    StringFromGUID2(reinterpret_cast<GUID&>(EventId),(LPOLESTR)strGuid, 64);
    // TODO: Display the message "IWMDMProgress3::Begin3 called." 
    // followed by the strGuid value.
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-begin">IWMDMProgress::Begin</a>