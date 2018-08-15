---
UID: NF:wmp.IWMPCdrom.eject
title: IWMPCdrom::eject
author: windows-sdk-content
description: The eject method ejects the CD or DVD from the drive.
old-location: wmp\iwmpcdrom_eject.htm
old-project: WMP
ms.assetid: 1b17c405-0887-4948-b375-c1ebcf2a72b3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPCdrom interface [Windows Media Player],eject method, IWMPCdrom.eject, IWMPCdrom::eject, IWMPCdromeject, eject, eject method [Windows Media Player], eject method [Windows Media Player],IWMPCdrom interface, wmp.iwmpcdrom_eject, wmp/IWMPCdrom::eject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPCdrom.eject
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdrom::eject


## -description



The <b>eject</b> method ejects the CD or DVD from the drive.




## -parameters






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
</table>
 




## -remarks



If the drive door is open, this method closes the door.

To use this method, read access to the library is required. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/323a6841-ffbd-4bbb-ac04-1d121cf5bd06">IWMPCdromInterface</a>



<a href="https://msdn.microsoft.com/cadac1c6-fff6-44aa-a6ce-2b2f69da2d78">IWMPCore::get_playState</a>



<a href="https://msdn.microsoft.com/07ca80a3-5175-4b1f-b83c-0df41a010cbf">IWMPSettings2::get_mediaAccessRights</a>



<a href="https://msdn.microsoft.com/925a4c0b-d613-4248-a341-bfc51d02cb85">IWMPSettings2::requestMediaAccessRights</a>
 

 

