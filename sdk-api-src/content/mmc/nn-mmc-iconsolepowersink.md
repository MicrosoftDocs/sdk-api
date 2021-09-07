---
UID: NN:mmc.IConsolePowerSink
title: IConsolePowerSink (mmc.h)
description: The IConsolePowerSink interface monitors and responds to power management messages.
helpviewer_keywords: ["IConsolePowerSink","IConsolePowerSink interface [MMC]","IConsolePowerSink interface [MMC]","described","_slate_iconsolepowersink","mmc.iconsolepowersink","mmc/IConsolePowerSink"]
old-location: mmc\iconsolepowersink.htm
tech.root: mmc
ms.assetid: dd23c6dc-9219-4d13-b237-13405a2fcb5a
ms.date: 12/05/2018
ms.keywords: IConsolePowerSink, IConsolePowerSink interface [MMC], IConsolePowerSink interface [MMC],described, _slate_iconsolepowersink, mmc.iconsolepowersink, mmc/IConsolePowerSink
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IConsolePowerSink
 - mmc/IConsolePowerSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IConsolePowerSink
---

# IConsolePowerSink interface


## -description

The 
<b>IConsolePowerSink</b> interface monitors and responds to power management messages.

## -inheritance

The <b>IConsolePowerSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConsolePowerSink</b> also has these types of members:

## -remarks

To receive power management notifications, your snap-in must use the <a href="/previous-versions/26k10xyy(v=vs.140)">AtlAdvise</a> function to associate an instance of the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsolepower">IConsolePower</a> interface with your implementation of the 
<b>IConsolePowerSink</b> interface. The following code example shows how to use the <a href="/previous-versions/26k10xyy(v=vs.140)">AtlAdvise</a> function.


#### Examples


```cpp
// Connect the IConsolePower and IConsolePowerSink interfaces.
// m_ipConsolePower is a pointer to an instance of 
// the IConsolePower interface.
// m_ipConsolePowerSink is a pointer to an instance of 
// the IConsolePowerSink interface.
// m_dwCookie is of type DWORD.
hr = AtlAdvise(m_ipConsolePower,
               m_ipConsolePowerSink,
               IID_IConsolePowerSink,
               &m_dwCookie);
```


When your snap-in closes or no longer requires power management notifications, call the <a href="/previous-versions/7s2bbwhc(v=vs.140)">AtlUnadvise</a> function to terminate the connection between the 
IConsolePower and 
IConsolePowerSink interfaces. The following code example shows how to use the <a href="/previous-versions/7s2bbwhc(v=vs.140)">AtlUnadvise</a> function.


```cpp
// Terminate the connection established previously.
hr = AtlUnadvise(m_ipConsolePower,
                 IID_IConsolePowerSink,
                 m_dwCookie);
```

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolepower">IConsolePower</a>
