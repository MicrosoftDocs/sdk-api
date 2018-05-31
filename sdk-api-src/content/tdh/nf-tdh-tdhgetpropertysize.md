---
UID: NF:tdh.TdhGetPropertySize
title: TdhGetPropertySize function
author: windows-sdk-content
description: Retrieves the size of one or more property values in the event data.
old-location: etw\tdhgetpropertysize_func.htm
old-project: ETW
ms.assetid: 52b034db-b08b-4c79-973f-33800ca866f5
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: TdhGetPropertySize, TdhGetPropertySize function [ETW], etw.tdhgetpropertysize_func, tdh.tdhgetpropertysize_func, tdh/TdhGetPropertySize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tdh.h
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
req.typenames: TEMPLATE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tdh.dll
-	API-MS-Win-Eventing-Tdh-L1-1-0.dll
-	MinTdh.dll
api_name:
-	TdhGetPropertySize
product: Windows
targetos: Windows
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TdhGetPropertySize function


## -description



		Retrieves the size of one or more property values in the event data.
		
		
	
	


## -parameters




### -param pEvent [in]

The event record passed to your <a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a> callback. For details, see the <a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a> structure.


### -param TdhContextCount [in]

Number of elements in <i>pTdhContext</i>.


### -param pTdhContext [in]

Array of context values for WPP or classic ETW events only, otherwise, <b>NULL</b>. For details, see the <a href="https://msdn.microsoft.com/184df0af-3ac5-406f-a298-4f23826ad85e">TDH_CONTEXT</a> structure.  The array must not contain duplicate context types.


### -param PropertyDataCount [in]

Number of data descriptor structures in <i>pPropertyData</i>.


### -param pPropertyData [in]

Array of <a href="https://msdn.microsoft.com/38e6f5b1-fce5-45e4-ac7a-09ba40d29837">PROPERTY_DATA_DESCRIPTOR</a> structures that define the property whose size you want to retrieve.

You can pass this same array  to the <a href="https://msdn.microsoft.com/3975792e-cc24-430a-914f-420f3a5ec1d6">TdhGetProperty</a> function to retrieve the property data.

If you are retrieving the size of a property that is not a member of a structure, you can specify a single data descriptor. If you are retrieving the size of a property that is a member of a structure, specify an array of two  data descriptors (structures cannot contain or reference other structures). For more information on specifying this parameter, see the example code below.


### -param pPropertySize [out]

Size of the property, in bytes. Use this value to allocate the buffer passed in the <i>pBuffer</i> parameter of the <a href="https://msdn.microsoft.com/3975792e-cc24-430a-914f-420f3a5ec1d6">TdhGetProperty</a> function.


## -returns



Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The schema for the event was not found or the specified map was not found.

If you used a MOF class to define your event, TDH looks for the schema in the WMI repository. If you used a manifest to define your event, TDH looks in the provider's resources. If you use a manifest, the <b>resourceFileName</b> attribute of the <b>provider</b> element defines the location where TDH expects to find the resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>resourceFileName</b> attribute in the manifest contains the location of the provider binary. When you register the manifest, the location is written to the registry. TDH was unable to find the binary based on the registered location.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_SERVER_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The WMI service is not available.

</td>
</tr>
</table>
 




## -remarks



If the event is a WPP or classic ETW event, you can specify context information that is used to help parse the event information. The event is a WPP event if the EVENT_HEADER_FLAG_TRACE_MESSAGE flag is set in the <b>Flags</b> member of <a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a> (see the <b>EventHeader</b> member of <a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a>). The event is a legacy ETW event if the EVENT_HEADER_FLAG_CLASSIC_HEADER flag is set.


#### Examples

For an example that shows how to call this function, see <a href="https://msdn.microsoft.com/16b36718-087f-4be9-9ca2-fc083358017b">Using TdhGetProperty to Consume Event Data</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3975792e-cc24-430a-914f-420f3a5ec1d6">TdhGetProperty</a>
 

 

