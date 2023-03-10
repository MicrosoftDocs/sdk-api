---
UID: NF:eaphostpeerconfigapis.EapHostPeerConfigBlob2Xml
title: EapHostPeerConfigBlob2Xml function (eaphostpeerconfigapis.h)
description: Converts the configuration BLOB to XML. (EapHostPeerConfigBlob2Xml)
helpviewer_keywords: ["EapHostPeerConfigBlob2Xml","EapHostPeerConfigBlob2Xml function [EAPHost]","eaphost.eaphostpeerconfigblob2xml","eaphostpeerconfigapis/EapHostPeerConfigBlob2Xml"]
old-location: eaphost\eaphostpeerconfigblob2xml.htm
tech.root: eaphost
ms.assetid: 158750ec-cc26-4740-add6-2135b9aa294c
ms.date: 12/05/2018
ms.keywords: EapHostPeerConfigBlob2Xml, EapHostPeerConfigBlob2Xml function [EAPHost], eaphost.eaphostpeerconfigblob2xml, eaphostpeerconfigapis/EapHostPeerConfigBlob2Xml
req.header: eaphostpeerconfigapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerConfigBlob2Xml
 - eaphostpeerconfigapis/EapHostPeerConfigBlob2Xml
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerConfigBlob2Xml
---

# EapHostPeerConfigBlob2Xml function


## -description

Converts the configuration BLOB to XML. 

The configuration BLOB is returned when the supplicant called one of the following methods.<ul>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob">EapHostPeerConfigXml2Blob</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui">EapHostPeerInvokeConfigUI</a>
</li>
<li>
<a href="/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult">EapHostPeerGetResult</a> - via the <a href="/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult">EapHostPeerMethodResult</a> structure</li>
</ul>

## -parameters

### -param dwFlags [in]

Not used. Set to 0.

### -param eapMethodType [in]

Refers to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type">EAP_METHOD_TYPE</a> structure that is referred to in the XML document.

### -param dwSizeOfConfigIn [in]

The size, in bytes, of the configuration BLOB.

### -param pConfigIn [in]

A pointer to a buffer that  contains the configuration BLOB to convert.  The buffer is of size <i>dwSizeOfConfigIn</i>.

### -param ppConfigDoc [out]

A pointer to a pointer to an XML document that  contains the converted configuration. If the EAP method does not support
                the [EapHostConfig Schema](/windows/win32/eaphost/eaphostconfigschema-schema) element.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



[EapHostPeerConfigXml2Blob](/windows/win32/eaphost/eaphostconfigschema-schema)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult">EapHostPeerGetResult</a>



<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui">EapHostPeerInvokeConfigUI</a>
