---
UID: NF:mswmdm.IWMDMProgress3.End3
title: IWMDMProgress3::End3 (mswmdm.h)
description: The End3 method is called by Windows Media Device Manager to indicate that an operation has finished.
helpviewer_keywords: ["End3","End3 method [windows Media Device Manager]","End3 method [windows Media Device Manager]","IWMDMProgress3 interface","IWMDMProgress3 interface [windows Media Device Manager]","End3 method","IWMDMProgress3.End3","IWMDMProgress3::End3","IWMDMProgress3End3","mswmdm/IWMDMProgress3::End3","wmdm.iwmdmprogress3_end3"]
old-location: wmdm\iwmdmprogress3_end3.htm
tech.root: WMDM
ms.assetid: fb09cfa8-1a96-412f-a97a-6cc1638b0c77
ms.date: 12/05/2018
ms.keywords: End3, End3 method [windows Media Device Manager], End3 method [windows Media Device Manager],IWMDMProgress3 interface, IWMDMProgress3 interface [windows Media Device Manager],End3 method, IWMDMProgress3.End3, IWMDMProgress3::End3, IWMDMProgress3End3, mswmdm/IWMDMProgress3::End3, wmdm.iwmdmprogress3_end3
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
 - IWMDMProgress3::End3
 - mswmdm/IWMDMProgress3::End3
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
 - IWMDMProgress3.End3
---

# IWMDMProgress3::End3


## -description

The <b>End3</b> method is called by Windows Media Device Manager to indicate that an operation has finished. This method extends <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress2-end2">IWMDMProgress2::End2</a> by providing additional input parameters for the identification (ID) of the event and for a pointer to the context of the commands.

## -parameters

### -param EventId [in]

A <b>GUID</b> specifying the event that is ending. Possible values are shown in the following table.

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

### -param hrCompletionCode [in]

<b>HRESULT</b> specifying the completion code of the operation that was in progress. The <i>hrCompletionCode</i> parameter is the return code of the operation that ended. This parameter can be any <b>HRESULT</b>, including standard COM error codes, Win32 error codes converted to <b>HRESULT</b>, or Windows Media Device Manager error codes.

### -param pContext [in, out]

Pointer to an <a href="/windows/desktop/WMDM/opaquecommand">OPAQUECOMMAND</a> structure containing a command sent directly to the device without being handled by Windows Media Device Manager. This parameter is optional and can be <b>NULL</b>. The context structure is a way for the component to send any relevant data with the event to the application. The component sending this structure should define how the application can interpret this data structure.

## -returns

Windows Media Device Manager ignores any return code returned by the <b>End3</b> method because the current operation is finished or cancelled before this method is called.

## -remarks

The interface that owns the method that is implementing an operation calls <b>End3</b> when the operation defined by the method is completed.


#### Examples

The following C++ code shows an example implementation of <b>End3</b>.


```cpp

HRESULT End3(GUID  EventId, HRESULT  hrCompletionCode, OPAQUECOMMAND*  pContext)
{
    // TODO: Display the message "IWMDMProgress3::End3 called."
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3">IWMDMProgress3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end">IWMDMProgress::End</a>