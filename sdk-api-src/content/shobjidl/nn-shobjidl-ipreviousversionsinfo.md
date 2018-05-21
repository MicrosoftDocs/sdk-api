---
UID: NN:shobjidl.IPreviousVersionsInfo
title: IPreviousVersionsInfo
author: windows-driver-content
description: Exposes a method that checks for previous versions of server files or folders, stored for the purpose of reversion by the shadow copies technology provided with Windows Server 2003.
old-location: shell\IPreviousVersionsInfo.htm
old-project: shell
ms.assetid: 5d55107e-a07a-4d70-80f6-7ec99578bb48
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IPreviousVersionsInfo, IPreviousVersionsInfo interface [Windows Shell], IPreviousVersionsInfo interface [Windows Shell],described, _shell_IPreviousVersionsInfo, shell.IPreviousVersionsInfo, shobjidl/IPreviousVersionsInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Twext.dll
api_name:
-	IPreviousVersionsInfo
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Twext.dll (version 5.2 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IPreviousVersionsInfo interface


## -description


Exposes a method that checks for previous versions of server files or folders, stored for the purpose of reversion by the <i>shadow copies</i> technology provided with Windows Server 2003.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPreviousVersionsInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPreviousVersionsInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPreviousVersionsInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03a0b218-4683-42b2-9080-9b92701dff1e">AreSnapshotsAvailable</a>
</td>
<td align="left" width="63%">
Queries for the availablilty of a Windows Server 2003 volume image recorded by the system at an earlier time.

</td>
</tr>
</table> 


## -remarks



The CLSID, IID, and definition for this interface are shown in the following example.

                

<pre class="syntax" xml:space="preserve"><code>// {596AB062-B4D2-4215-9F74-E9109B0A8153}
const CLSID CLSID_PreviousVersions = {0x596AB062, 0xB4D2, 0x4215, 
                             {0x9F, 0x74, 0xE9, 0x10, 0x9B, 0x0A, 0x81, 0x53}};

// {76e54780-ad74-48e3-a695-3ba9a0aff10d}
const IID IID_IPreviousVersionsInfo = {0x76E54780, 0xAD74, 0x48E3, 
                             {0xA6, 0x95, 0x3B, 0xA9, 0xA0, 0xAF, 0xF1, 0x0D}};

MIDL_INTERFACE("76e54780-ad74-48e3-a695-3ba9a0aff10d")
IPreviousVersionsInfo : public IUnknown
{
public:
    virtual HRESULT STDMETHODCALLTYPE AreSnapshotsAvailable( 
        /* [string][in] */ LPCWSTR pszPath,
        /* [in] */ BOOL fOkToBeSlow,
        /* [retval][out] */ BOOL *pfAvailable) = 0;
};</code></pre>
Note that the shadow copies technology does not store entire copies of older versions unless they are deleted; only the changed bits are stored.



