---
UID: NF:vidcap.IKsTopologyInfo.get_NodeName
title: IKsTopologyInfo::get_NodeName (vidcap.h)
description: The get_NodeName method returns the name of the node.
helpviewer_keywords: ["IKsTopologyInfo interface [DirectShow]","get_NodeName method","IKsTopologyInfo.get_NodeName","IKsTopologyInfo::get_NodeName","IKsTopologyInfoget_NodeName","dshow.ikstopologyinfo_get_nodename","get_NodeName","get_NodeName method [DirectShow]","get_NodeName method [DirectShow]","IKsTopologyInfo interface","vidcap/IKsTopologyInfo::get_NodeName"]
old-location: dshow\ikstopologyinfo_get_nodename.htm
tech.root: dshow
ms.assetid: 3e24ef6f-e49d-4397-a9b8-a46fcf576a01
ms.date: 4/26/2023
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NodeName method, IKsTopologyInfo.get_NodeName, IKsTopologyInfo::get_NodeName, IKsTopologyInfoget_NodeName, dshow.ikstopologyinfo_get_nodename, get_NodeName, get_NodeName method [DirectShow], get_NodeName method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NodeName
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKsTopologyInfo::get_NodeName
 - vidcap/IKsTopologyInfo::get_NodeName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsTopologyInfo.get_NodeName
---

# IKsTopologyInfo::get_NodeName


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_NodeName</code> method returns the name of the node.

## -parameters

### -param dwNodeId [in]

Index of the node. To find the number of nodes, call the <a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_numnodes">IKsTopologyInfo::get_NumNodes</a> method.

### -param pwchNodeName [out]

Pointer to a wide-character array that receives the name. To find the required buffer size, set this parameter to <b>NULL</b>. The size is returned in the <i>pdwNameLen</i> parameter.

### -param dwBufSize [in]

Size of the <i>pwchNodeName</i> array, in bytes.

### -param pdwNameLen [out]

Receives the buffer size required to hold the name, in bytes. This parameter cannot be <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WIN32_FROM_HRESULT(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough.

</td>
</tr>
</table>

## -remarks

To find the buffer size for the name, call the method once with <b>NULL</b> for the <i>pwchNodeName</i> parameter and zero for the <i>dwBufSize</i> parameter. The method returns the buffer size in <i>pdwNameLen</i>. The method's return value, in this case, is HRESULT_FROM_WIN32(ERROR_MORE_DATA). Then allocate the array and call the method again.


#### Examples


```cpp

// pKsTopo is an IKsTopologyInfo pointer.
// iNode is the index of a node.
DWORD cbName = 0;
hr = pKsTopo->get_NodeName(iNode, NULL, 0, &cbName);
if (hr == HRESULT_FROM_WIN32(ERROR_MORE_DATA))
{
    if (cbName > sizeof(WCHAR))
    {
        WCHAR *nodeName = new WCHAR[cbName / sizeof(WCHAR)];
        if (nodeName == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            hr = pKsTopo->get_NodeName(iNode, nodeName, cbName, &cbName);
            /* ... */
            delete [] nodeName;
        }
    }
}

```

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/ms785846(v=vs.85)">IKsTopologyInfo Interface</a>