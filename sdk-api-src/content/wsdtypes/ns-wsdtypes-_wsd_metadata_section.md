---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _WSD_METADATA_SECTION structure


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
The metadata section contains model-specific information relating to the device. If the <b>Data</b> member is specified, then its type is <a href="https://msdn.microsoft.com/614daaeb-76ac-4dec-93fe-f413164d5330">WSD_THIS_MODEL_METADATA</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_ThisDevice"></a><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_thisdevice"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2006_02_DEVPROF_THISDEVICE"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice</b></dt>
</dl>
</td>
<td width="60%">
The metadata section contains metadata that is unique to a specific device. If the <b>Data</b> member is specified, then its type is <a href="https://msdn.microsoft.com/7b9d063f-f0d5-4333-a5d8-e9a6d2d9af88">WSD_THIS_DEVICE_METADATA</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_Relationship"></a><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_relationship"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2006_02_DEVPROF_RELATIONSHIP"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship</b></dt>
</dl>
</td>
<td width="60%">
The metadata section contains metadata about the relationship between two or more services. If the <b>Data</b> member is specified, then its type is <a href="https://msdn.microsoft.com/232ea033-f368-4a37-9bec-ba5dc0d9b60f">WSD_RELATIONSHIP_METADATA</a>.


</td>
</tr>
</table>
 


### -field Identifier

The dialect-specific identifier for the scope/domain/namespace of the metadata section.


### -field Data

Reference to a binary representation of the metadata. The type of metadata is specified by <b>Dialect</b>. This member is ignored if <b>Dialect</b> does not have a value of http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel, http://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice, or http://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship.


### -field MetadataReference

Reference to a <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a> structure used identify the endpoint from which metadata can be retrieved. 


### -field Location

A URI that specifies the location from which metadata can be retrieved.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

