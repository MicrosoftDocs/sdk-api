---
UID: NF:ehstorapi.IEnhancedStorageSilo.SendCommand
title: IEnhancedStorageSilo::SendCommand (ehstorapi.h)
description: Sends a raw silo command to the silo object. This method is utilized to communicate with a silo which is not represented by a driver.
helpviewer_keywords: ["IEnhancedStorageSilo interface [Enhanced Storage]","SendCommand method","IEnhancedStorageSilo.SendCommand","IEnhancedStorageSilo::SendCommand","SendCommand","SendCommand method [Enhanced Storage]","SendCommand method [Enhanced Storage]","IEnhancedStorageSilo interface","ehstorapi/IEnhancedStorageSilo::SendCommand","enstor.ienhancedstoragesilo_sendcommand"]
old-location: enstor\ienhancedstoragesilo_sendcommand.htm
tech.root: enstor
ms.assetid: 8b52815e-e100-4c25-b7d3-8469d1dad745
ms.date: 12/05/2018
ms.keywords: IEnhancedStorageSilo interface [Enhanced Storage],SendCommand method, IEnhancedStorageSilo.SendCommand, IEnhancedStorageSilo::SendCommand, SendCommand, SendCommand method [Enhanced Storage], SendCommand method [Enhanced Storage],IEnhancedStorageSilo interface, ehstorapi/IEnhancedStorageSilo::SendCommand, enstor.ienhancedstoragesilo_sendcommand
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
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
 - IEnhancedStorageSilo::SendCommand
 - ehstorapi/IEnhancedStorageSilo::SendCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EhStorAPI.h
api_name:
 - IEnhancedStorageSilo.SendCommand
---

# IEnhancedStorageSilo::SendCommand


## -description

Sends a raw silo command to the silo object. This method is utilized to communicate with a silo which is not represented by a driver.

## -parameters

### -param Command [in]

The silo command to be issued. 8 bits of this value are placed in the byte at position 3 of the CDB sent to the device; i.e. the second byte of the <b>SecurityProtocolSpecific</b> field.

### -param pbCommandBuffer [in]

The command payload sent to the device in the send data phase of the command.

### -param cbCommandBuffer [in]

The count of bytes contained in the <i>pbCommandBuffer</i> buffer.

### -param pbResponseBuffer [out]

The response payload that is returned to the host from the device in the receive data phase of the command.

### -param pcbResponseBuffer [out]

On method entry, contains the size of <i>pbResponseBuffer</i> in bytes. On method exit, it contains the count of bytes contained in the returned <i>pbResponse</i> buffer.

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
Silo command completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The pbCommandBuffer, pbResponseBuffer, or pcbResponseBuffer parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_ENOUGH_MEMORY)</b></dt>
</dl>
</td>
<td width="60%">
The size of pbResponseBuffer is insufficient to contain the response data.

</td>
</tr>
</table>

## -remarks

This method is currently not supported by the IEEE 1667 certificate and password silos. It is recommended that the <a href="/previous-versions/windows/desktop/enstor/enhanced-storage-portable-device-commands">Enhanced Storage Portable Device Commands</a> are used instead.

The caller is responsible for sending correct parameters to the command, as well as allocating the necessary buffer for the returned results.

## -see-also

<a href="/previous-versions/windows/desktop/enstor/enhanced-storage-portable-device-commands">Enhanced Storage Portable Device Commands</a>



<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a>