---
UID: NF:mbnapi.IMbnInterface.GetSubscriberInformation
title: IMbnInterface::GetSubscriberInformation (mbnapi.h)
description: Gets the subscriber information.
helpviewer_keywords: ["GetSubscriberInformation","GetSubscriberInformation method [Microsoft Broadband Networks]","GetSubscriberInformation method [Microsoft Broadband Networks]","IMbnInterface interface","IMbnInterface interface [Microsoft Broadband Networks]","GetSubscriberInformation method","IMbnInterface.GetSubscriberInformation","IMbnInterface::GetSubscriberInformation","mbn.imbninterface_getsubscriberinformation","mbnapi/IMbnInterface::GetSubscriberInformation"]
old-location: mbn\imbninterface_getsubscriberinformation.htm
tech.root: mbn
ms.assetid: 9114a3ed-2dc9-4637-b3d5-9430d309e89b
ms.date: 12/05/2018
ms.keywords: GetSubscriberInformation, GetSubscriberInformation method [Microsoft Broadband Networks], GetSubscriberInformation method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetSubscriberInformation method, IMbnInterface.GetSubscriberInformation, IMbnInterface::GetSubscriberInformation, mbn.imbninterface_getsubscriberinformation, mbnapi/IMbnInterface::GetSubscriberInformation
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnInterface::GetSubscriberInformation
 - mbnapi/IMbnInterface::GetSubscriberInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnInterface.GetSubscriberInformation
---

# IMbnInterface::GetSubscriberInformation


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the subscriber information.

## -parameters

### -param subscriberInformation [out, retval]

A pointer to the address of an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsubscriberinformation">IMbnSubscriberInformation</a> interface that contains subscriber information for the device.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.

## -returns

This method can return one of these values.

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
The method completed successfully.  <i>subscriberInformation</i> contains a valid interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband  service is currently probing for the information.  The calling application can get notified when the information is available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onsubscriberinformationchange">OnSubscriberInformationChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

</td>
</tr>
</table>

## -remarks

The <b>GetSubscriberInformation</b> method returns the subscriber-related information, including subscriber ID, SIM international circuit card number, and phone numbers associated with this interface.

When this method is called from a Windows Store app with mobile operator privileges  it will only return the SIM International circuit card number defined by   the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid">SimIccID</a> property.

Some of the values returned in subscriber information are populated only when the ready state which as reported by the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getreadystate">GetReadyState</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> is <b>MBN_READY_STATE_INITIALIZED</b>. Whenever there is a change in the subscriber information associated with the Mobile Broadband device, the Mobile Broadband service will notify registered applications by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onsubscriberinformationchange">OnSubscriberInformationChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

Subscriber information for a device will not change once the device ready state is <b>MBN_READY_STATE_INITIALIZED</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>