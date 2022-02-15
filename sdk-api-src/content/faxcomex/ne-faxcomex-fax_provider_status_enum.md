---
UID: NE:faxcomex.FAX_PROVIDER_STATUS_ENUM
title: FAX_PROVIDER_STATUS_ENUM (faxcomex.h)
description: The FAX_PROVIDER_STATUS_ENUM enumeration defines the status values for a fax extension (a fax service provider (FSP) or a fax inbound routing extension).
helpviewer_keywords: ["FAX_PROVIDER_STATUS_ENUM","FAX_PROVIDER_STATUS_ENUM enumeration [Fax Service]","_mfax_fax_provider_status_enum","fax._mfax_fax_provider_status_enum","faxcomex/FAX_PROVIDER_STATUS_ENUM","faxcomex/fpsBAD_GUID","faxcomex/fpsBAD_VERSION","faxcomex/fpsCANT_INIT","faxcomex/fpsCANT_LINK","faxcomex/fpsCANT_LOAD","faxcomex/fpsSERVER_ERROR","faxcomex/fpsSUCCESS","fpsBAD_GUID","fpsBAD_VERSION","fpsCANT_INIT","fpsCANT_LINK","fpsCANT_LOAD","fpsSERVER_ERROR","fpsSUCCESS"]
old-location: fax\_mfax_fax_provider_status_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8ejx.htm
ms.date: 12/05/2018
ms.keywords: FAX_PROVIDER_STATUS_ENUM, FAX_PROVIDER_STATUS_ENUM enumeration [Fax Service], _mfax_fax_provider_status_enum, fax._mfax_fax_provider_status_enum, faxcomex/FAX_PROVIDER_STATUS_ENUM, faxcomex/fpsBAD_GUID, faxcomex/fpsBAD_VERSION, faxcomex/fpsCANT_INIT, faxcomex/fpsCANT_LINK, faxcomex/fpsCANT_LOAD, faxcomex/fpsSERVER_ERROR, faxcomex/fpsSUCCESS, fpsBAD_GUID, fpsBAD_VERSION, fpsCANT_INIT, fpsCANT_LINK, fpsCANT_LOAD, fpsSERVER_ERROR, fpsSUCCESS
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: FAX_PROVIDER_STATUS_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_PROVIDER_STATUS_ENUM
 - faxcomex/FAX_PROVIDER_STATUS_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_PROVIDER_STATUS_ENUM
---

# FAX_PROVIDER_STATUS_ENUM enumeration


## -description

The <b>FAX_PROVIDER_STATUS_ENUM</b> enumeration defines the status values for a fax extension (a fax service provider (FSP) or a fax inbound routing extension).

## -enum-fields

### -field fpsSUCCESS:0

The extension loaded, linked, and initialized successfully.

### -field fpsSERVER_ERROR

A server-related error occurred while the fax service was trying to load, link, and initialize the extension; for example, there may have been insufficient memory resources. Call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider-initerrorcode-vb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-initerrorcode-vb">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.

### -field fpsBAD_GUID

An error occurred while the fax service was parsing the extension's installation data; the extension's GUID is invalid. Refer to the <b>InitErrorCode</b> property to get the error code.

### -field fpsBAD_VERSION

An error occurred while the fax service was parsing the extension's installation data; the extension reports an invalid version of the FSP or routing extension API; the routing extension is the non-default MS routing extension for a desktop computer installation. Call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider-initerrorcode-vb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-initerrorcode-vb">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.

### -field fpsCANT_LOAD

An error occurred while the fax service was loading the FSP or routing extension's DLL. Call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider-initerrorcode-vb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-initerrorcode-vb">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.

### -field fpsCANT_LINK

An error occurred when the fax service attempted to dynamically link to one of the functions that the FSP or routing extension's DLL must export. Call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider-initerrorcode-vb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-initerrorcode-vb">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.

### -field fpsCANT_INIT

An error occurred when the fax service called the extension's initialization function. For virtual devices, the <b>InitErrorCode</b> property is an <b>HRESULT</b> value; otherwise, it is a Win32 error code. Call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider-initerrorcode-vb">IFaxDeviceProvider::get_InitErrorCode</a> method or the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-initerrorcode-vb">IFaxInboundRoutingExtension::get_InitErrorCode</a> method to return the last error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxdeviceprovider-get_status">IFaxDeviceProvider::get_Status</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-status-vb">IFaxInboundRoutingExtension::get_Status</a>
