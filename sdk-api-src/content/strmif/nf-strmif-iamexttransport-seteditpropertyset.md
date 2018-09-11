---
UID: NF:strmif.IAMExtTransport.SetEditPropertySet
title: IAMExtTransport::SetEditPropertySet
author: windows-sdk-content
description: The SetEditPropertySet method registers an edit property set that describes a group of edit properties.
old-location: dshow\iamexttransport_seteditpropertyset.htm
tech.root: DirectShow
ms.assetid: 40695c7c-7381-44c0-b41f-7c838c9c83b5
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMExtTransport interface [DirectShow],SetEditPropertySet method, IAMExtTransport.SetEditPropertySet, IAMExtTransport::SetEditPropertySet, IAMExtTransportSetEditPropertySet, SetEditPropertySet, SetEditPropertySet method [DirectShow], SetEditPropertySet method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_seteditpropertyset, strmif/IAMExtTransport::SetEditPropertySet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtTransport.SetEditPropertySet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtTransport::SetEditPropertySet


## -description



The <code>SetEditPropertySet</code> method registers an edit property set that describes a group of edit properties.



This method is not implemented.


## -parameters




### -param pEditID [in, out]

Pointer to a <b>long</b> integer that specifies or receives an identifier for the edit property set.


### -param State [in]

Specifies the state of the edit property set.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_ACTIVE</td>
<td>Activates the edit property set.</td>
</tr>
<tr>
<td>ED_DELETE</td>
<td>Deletes the edit property set.</td>
</tr>
<tr>
<td>ED_INACTIVE</td>
<td>Inactivates edit property set.</td>
</tr>
<tr>
<td>ED_REGISTER</td>
<td>Registers the edit property set.</td>
</tr>
</table>
 

If the value is ED_REGISTER, the <i>pEditID</i> parameter receives an identifier for the edit property set. For the other flags, use the <i>pEditID</i> parameter to specify the identifier.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



An <i>edit event</i> is a set of parameters that define a recording sequence. For example, the parameters can specify editing modes, inpoints and outpoints, or seek positions. Each edit event consists of one or more parameters, called <i>edit properties</i>. The collection of properties is called an <i>edit property set</i>. Each edit property set is identified by a <b>long</b> integer, assigned by the device filter.

To create and execute an edit event, the application must do the following:

<ul>
<li>Register an edit property set. Call the <code>SetEditPropertySet</code> method with the value ED_REGISTER in the <i>State</i> parameter. When the method returns, the <i>pEditID</i> parameter contains the identifier for the edit property set. Use this number to identify the edit property set in subsequent method calls.</li>
<li>Specify the edit properties using the <a href="https://msdn.microsoft.com/85ac14c7-7b47-4462-98ba-68a73f4c7497">IAMExtTransport::SetEditProperty</a> method.</li>
<li>Activate the edit event by calling <code>SetEditPropertySet</code> with the value ED_ACTIVE.</li>
<li>Cue the transport by calling <code>SetEditProperty</code> with the value ED_EDIT_SEEK.</li>
<li>Run the filter graph.</li>
</ul>
For example, the following code configures an insert edit on all tracks:


```cpp

// Register an edit property set ID. (Causes memory to be allocated.)
long EditId;
SetEditPropertySet(&EditId, ED_REGISTER);  

// Set the edit mode.
SetEditProperty(EditId, ED_EDIT_MODE, ED_EDIT_MODE_INSERT);
// Set the particulars about the event.
SetEditProperty(EditId, ED_EDIT_TRACK, ED_VIDEO | ED_AUDIO_ALL);
SetEditProperty(EditId, ED_REHEARSE_MODE, ED_EDIT_PERFORM);

// Set the source and record times. 
SetEditProperty(EditId, ED_EDIT_SRC_INPOINT, 200)
SetEditProperty(EditId, ED_EDIT_SRC_OUTPOINT, 500)
SetEditProperty(EditId, ED_EDIT_REC_INPOINT, 100)
SetEditProperty(EditId, ED_EDIT_REC_OUTPOINT, 400)

// Activate the edit event.
SetEditPropertySet(&EditId, ED_ACTIVE); 
// Cue up the machine.
SetEditProperty(EditId, ED_EDIT_SEEK, OATRUE); 

// Run the graph. (Not shown.)

```


<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/1afb45da-947c-454d-8be9-46ac58802b9e">IAMExtTransport::GetEditPropertySet</a>
 

 

