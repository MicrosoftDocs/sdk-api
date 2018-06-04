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

# IFaxTiff interface


## -description


The <b>IFaxTiff</b> dual interface is used by a fax client application to retrieve information about <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> objects. A FaxTiff object represents a Tagged Image File Format Class F (TIFF Class F) file that the fax service has transmitted or received. The fax service embeds custom Tagged Image File Format (TIFF) tags in the file to store information about the fax transmission.

It is not necessary to be familiar with the structure of a TIFF file to use the <b>IFaxTiff</b> interface and access the attributes of <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> objects. This interface provides a convenient alternative to manually parsing the TIFF data in a fax file. The <b>IFaxTiff</b> interface includes the following property methods:
<ul>
<li>Property methods to set and retrieve the name of the fax file described by the <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object.</li>
<li>Property methods to retrieve other attributes of the <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object, such as device and station identifiers, the fax number, and sender and recipient names.</li>
</ul><div class="alert"><b>Note</b>  A fax client application must  set the <a href="https://msdn.microsoft.com/c993c276-eb77-4173-bfc5-0c82decb2b52">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object.</div><div> </div>

## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

            You should not implement this interface. The Microsoft standard implementation provides complete functionality.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>

            Use the <b>IFaxTiff</b> interface to retrieve the properties of a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object.

Call the <a href="_com_CoCreateInstance">CoCreateInstance</a> function to retrieve a pointer to an <b>IFaxTiff</b> interface and create an instance of a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object. It is not necessary to call the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method to initiate a connection with an active fax server. A fax server connection is not required to access the <b>IFaxTiff</b> interface.

The property methods of the <b>IFaxTiff</b> interface get or set the properties described following. If the property supports read access, the <b>IFaxTiff</b> interface includes a <i>get_PropertyName</i> method. If the property supports write access, the interface includes a <i>put_PropertyName</i> method.

Following are the properties associated with a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object. 




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

