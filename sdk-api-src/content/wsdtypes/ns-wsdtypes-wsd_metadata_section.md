---
UID: NS:wsdtypes._WSD_METADATA_SECTION
title: WSD_METADATA_SECTION (wsdtypes.h)
description: Represents a section of metadata in a generic form.
helpviewer_keywords: ["WSD_METADATA_SECTION","WSD_METADATA_SECTION structure","http://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship","http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice","http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel","ncd.wsd_metadata_section_struct","wsdtypes/WSD_METADATA_SECTION"]
old-location: ncd\wsd_metadata_section_struct.htm
tech.root: ncd
ms.assetid: e3e39d0a-6fb1-4cb9-b399-6ffe0e73ba91
ms.date: 12/05/2018
ms.keywords: WSD_METADATA_SECTION, WSD_METADATA_SECTION structure, http://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship, http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice, http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel, ncd.wsd_metadata_section_struct, wsdtypes/WSD_METADATA_SECTION
req.header: wsdtypes.h
req.include-header: Wsdapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSD_METADATA_SECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_METADATA_SECTION
 - wsdtypes/_WSD_METADATA_SECTION
 - WSD_METADATA_SECTION
 - wsdtypes/WSD_METADATA_SECTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_METADATA_SECTION
---

# WSD_METADATA_SECTION structure


## -description

Represents a section of metadata in a generic form.


<div class="alert"><b>Note</b>  Only one of the <b>Data</b>, <b>MetadataReference</b>, or <b>Location</b> members should be specified.</div><div> </div>

## -struct-fields

### -field Dialect

The format and version of the metadata section.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_ThisModel"></a><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_thismodel"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2006_02_DEVPROF_THISMODEL"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel</b></dt>
</dl>
</td>
<td width="60%">
The metadata section contains model-specific information relating to the device. If the <b>Data</b> member is specified, then its type is <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_model_metadata">WSD_THIS_MODEL_METADATA</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_ThisDevice"></a><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_thisdevice"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2006_02_DEVPROF_THISDEVICE"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice</b></dt>
</dl>
</td>
<td width="60%">
The metadata section contains metadata that is unique to a specific device. If the <b>Data</b> member is specified, then its type is <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_device_metadata">WSD_THIS_DEVICE_METADATA</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_Relationship"></a><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_relationship"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2006_02_DEVPROF_RELATIONSHIP"></a><dl>
<dt><b>`http://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship`</b></dt>
</dl>
</td>
<td width="60%">
The metadata section contains metadata about the relationship between two or more services. If the <b>Data</b> member is specified, then its type is <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_relationship_metadata">WSD_RELATIONSHIP_METADATA</a>.


</td>
</tr>
</table>

### -field Identifier

The dialect-specific identifier for the scope/domain/namespace of the metadata section.

### -field Data

Reference to a binary representation of the metadata. The type of metadata is specified by <b>Dialect</b>. This member is ignored if <b>Dialect</b> does not have a value of `http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel`, `http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice`, or `http://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship`.

### -field MetadataReference

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a> structure used identify the endpoint from which metadata can be retrieved.

### -field Location

A URI that specifies the location from which metadata can be retrieved.

### -field Any

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.