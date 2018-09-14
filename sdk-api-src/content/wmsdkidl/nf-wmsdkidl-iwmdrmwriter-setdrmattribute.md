---
UID: NF:wmsdkidl.IWMDRMWriter.SetDRMAttribute
title: IWMDRMWriter::SetDRMAttribute
author: windows-sdk-content
description: The SetDRMAttribute method sets DRM-header attributes as well as other DRM run-time properties.
old-location: wmformat\iwmdrmwriter_setdrmattribute.htm
tech.root: wmformat
ms.assetid: f54bba2a-872e-4ed1-b2c6-3e6b85a48df6
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMDRMWriter interface [windows Media Format],SetDRMAttribute method, IWMDRMWriter.SetDRMAttribute, IWMDRMWriter::SetDRMAttribute, IWMDRMWriterSetDRMAttribute, SetDRMAttribute, SetDRMAttribute method [windows Media Format], SetDRMAttribute method [windows Media Format],IWMDRMWriter interface, wmformat.iwmdrmwriter_setdrmattribute, wmsdkidl/IWMDRMWriter::SetDRMAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMWriter.SetDRMAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDRMWriter::SetDRMAttribute


## -description


<p class="CCE_Message">[<b>SetDRMAttribute</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>SetDRMAttribute</b> method sets DRM-header attributes as well as other DRM run-time properties.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number to which the attribute applies.


### -param pszName [in]

Pointer to a null-terminated string containing the attribute name. See Remarks for supported attributes.


### -param Type [in]

A value from the <a href="https://msdn.microsoft.com/2a2756f9-2d76-48c9-bbea-35ee33a39918">WMT_ATTR_DATATYPE</a> enumeration type specifying the data type of the attribute data.


### -param pValue [in]

Pointer to an array of bytes containing the attribute data.


### -param cbLength [in]

The size, in bytes, of the attribute data pointed to by <i>pValue</i>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method is somewhat misnamed because it is used to set not only writable DRM file attributes (See <a href="https://msdn.microsoft.com/222ef91c-b776-4de8-b1ad-88c2beca05aa">DRM Attribute List</a>), but also certain DRM properties that are used by the DRM run-time components but are not written to the DRM header in the file. (See <a href="https://msdn.microsoft.com/862fc8bc-6e40-4496-862a-c12c8a382116">DRM Properties</a>.)

The properties <b>Use_Advanced_DRM</b> and <b>Use_DRM</b> may be specified before a profile is set. No other properties can be set before a profile is set. The following code snippet shows how to call this function, using the <a href="https://msdn.microsoft.com/111765f6-963c-477d-8224-8e4fa06b0cc3">DRM_ContentID</a> property as an example. Assume that <i>pDRMWriter</i> is a <b>IWMDRMWriter</b> interface pointer, and <i>wszContentID</i> is an array of type <b>WCHAR</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
hr = pDRMWriter-&gt;SetDRMAttribute( 0, g_wszWMDRM_ContentID, 
        WMT_TYPE_STRING, (BYTE *)wszContentID, 
        ( wcslen( wszContentID ) + 1 ) * sizeof( WCHAR ) );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/222ef91c-b776-4de8-b1ad-88c2beca05aa">DRM Attribute List</a>



<a href="https://msdn.microsoft.com/862fc8bc-6e40-4496-862a-c12c8a382116">DRM Properties</a>



<a href="https://msdn.microsoft.com/fd466cf8-b1f8-49aa-a486-8fd347b29178">IWMDRMWriter Interface</a>
 

 

