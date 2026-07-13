---
UID: NF:strmif.IAMExtTransport.SetEditPropertySet
title: IAMExtTransport::SetEditPropertySet (strmif.h)
description: The SetEditPropertySet method registers an edit property set that describes a group of edit properties.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","SetEditPropertySet method","IAMExtTransport.SetEditPropertySet","IAMExtTransport::SetEditPropertySet","IAMExtTransportSetEditPropertySet","SetEditPropertySet","SetEditPropertySet method [DirectShow]","SetEditPropertySet method [DirectShow]","IAMExtTransport interface","dshow.iamexttransport_seteditpropertyset","strmif/IAMExtTransport::SetEditPropertySet"]
old-location: dshow\iamexttransport_seteditpropertyset.htm
tech.root: dshow
ms.assetid: 40695c7c-7381-44c0-b41f-7c838c9c83b5
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],SetEditPropertySet method, IAMExtTransport.SetEditPropertySet, IAMExtTransport::SetEditPropertySet, IAMExtTransportSetEditPropertySet, SetEditPropertySet, SetEditPropertySet method [DirectShow], SetEditPropertySet method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_seteditpropertyset, strmif/IAMExtTransport::SetEditPropertySet
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMExtTransport::SetEditPropertySet
 - strmif/IAMExtTransport::SetEditPropertySet
dev_langs:
 - c++
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
---

# IAMExtTransport::SetEditPropertySet


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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
<li>Specify the edit properties using the <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-seteditproperty">IAMExtTransport::SetEditProperty</a> method.</li>
<li>Activate the edit event by calling <code>SetEditPropertySet</code> with the value ED_ACTIVE.</li>
<li>Cue the transport by calling <code>SetEditProperty</code> with the value ED_EDIT_SEEK.</li>
<li>Run the filter graph.</li>
</ul>
For example, the following code configures an insert edit on all tracks:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Register an edit property set ID. (Causes memory to be allocated.)
long EditId;
SetEditPropertySet(&amp;EditId, ED_REGISTER);  

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
SetEditPropertySet(&amp;EditId, ED_ACTIVE); 
// Cue up the machine.
SetEditProperty(EditId, ED_EDIT_SEEK, OATRUE); 

// Run the graph. (Not shown.)
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-geteditpropertyset">IAMExtTransport::GetEditPropertySet</a>