---
UID: NF:eaphostpeerconfigapis.EapHostPeerConfigXml2Blob
title: EapHostPeerConfigXml2Blob function (eaphostpeerconfigapis.h)
author: windows-sdk-content
description: Converts XML into the configuration BLOB.
old-location: eaphost\eaphostpeerconfigxml2blob.htm
tech.root: eaphost
ms.assetid: 728fab9e-6aa4-49c0-ab1f-89686543524c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostPeerConfigXml2Blob, EapHostPeerConfigXml2Blob function [EAPHost], eaphost.eaphostpeerconfigxml2blob, eaphostpeerconfigapis/EapHostPeerConfigXml2Blob
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerConfigXml2Blob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapHostPeerConfigXml2Blob function


## -description


 Converts XML into the configuration  BLOB.  When the supplicant starts authentication or calls <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui">EapHostPeerInvokeConfigUI</a>, the supplicant calls <b>EapHostPeerConfigXml2Blob</b> to convert the XML configuration into a BLOB. 

The XML data to be converted could originate  from a <b>EapHostPeerConfigBlob2Xml</b> call, or the data could originate from a XML created by a system administrator or other XML author. 


## -parameters




### -param dwFlags [in]

Not used. Set to 0.


### -param pConfigDoc [in]

Sends a pointer to the XML configuration to be converted.


### -param pdwSizeOfConfigOut [out]

A pointer to the size, in bytes, of the configuration BLOB.


### -param ppConfigOut [out]

A pointer to a pointer to a byte buffer that contains the configuration data converted from XML. The configuration data is created inside <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eaphostconfigschema-schema">EapHostConfig Schema</a> element. The buffer is of size <i>pdwSizeOfConfigOut</i>. After consuming the data, this memory must be freed by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>.  


### -param pEapMethodType [out]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_method_type">EAP_METHOD_TYPE</a> structure referred to in the XML document. 


### -param ppEapError [out]

A pointer a pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structure that contains any errors raised  by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-configuration-functions">EAPHost Supplicant Configuration Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob">EapHostPeerConfigXml2Blob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult">EapHostPeerGetResult</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui">EapHostPeerInvokeConfigUI</a>
 

 

