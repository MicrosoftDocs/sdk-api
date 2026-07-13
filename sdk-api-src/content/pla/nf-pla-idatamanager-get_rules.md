---
UID: NF:pla.IDataManager.get_Rules
title: IDataManager::get_Rules (pla.h)
description: Retrieves or sets the rules to apply to the report. (Get)
helpviewer_keywords: ["IDataManager interface [PLA]","Rules property","IDataManager.Rules","IDataManager.get_Rules","IDataManager::Rules","IDataManager::get_Rules","IDataManager::put_Rules","Rules property [PLA]","Rules property [PLA]","IDataManager interface","base.idatamanager_rules","get_Rules","pla.idatamanager_rules","pla/IDataManager::Rules","pla/IDataManager::get_Rules","pla/IDataManager::put_Rules"]
old-location: pla\idatamanager_rules.htm
tech.root: PLA
ms.assetid: 17403e57-2eea-4a2b-a75c-66f486622078
ms.date: 12/05/2018
ms.keywords: IDataManager interface [PLA],Rules property, IDataManager.Rules, IDataManager.get_Rules, IDataManager::Rules, IDataManager::get_Rules, IDataManager::put_Rules, Rules property [PLA], Rules property [PLA],IDataManager interface, base.idatamanager_rules, get_Rules, pla.idatamanager_rules, pla/IDataManager::Rules, pla/IDataManager::get_Rules, pla/IDataManager::put_Rules
req.header: pla.h
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
req.lib: 
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataManager::get_Rules
 - pla/IDataManager::get_Rules
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataManager.Rules
 - IDataManager.get_Rules
 - IDataManager.put_Rules
---

# IDataManager::get_Rules


## -description

Retrieves or sets the rules to apply to the report. 

This property is read/write.

## -parameters

## -remarks

The rules modify  the contents of the report after it is generated. To specify the content that TraceRpt generates, see <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatamanager-get_reportschema">IDataManager::ReportSchema</a>.

The following schema defines the rules that you can specify. The <b>Rules</b> element is the root node. You can specify one or more <b>Group</b> elements, and each <b>Group</b> element can contain one or more <b>Rule</b> elements. The <b>Help</b> element is an optional user-defined element. The <b>Step</b> element defines a set of conditions and associated actions that are taken if the conditions are met.


```xml
<Rules>
    <Include name="" fatal="true|false"/>
    <Group name="" enabled="true|false">
        <Rule name="" enabled="true|false">
            <Help/>
            <Step/>
        </Rule>
    </Group>
</Rules>

```



```xml
<Step select="" fatal="true|false" sortType="first|max|min" sortValue="" sortDataType="">
    <UserInput/>
    <Exists>
        <When/>
        <Otherwise/>
    </Exists>
    <Otherwise/>
</Step>

```



```xml
<UserInput name="" expression="">
    <Description/>
</UserInput>

```



```xml
<When expression="" matchRE="">
    <Action/>
</When>
...
<Otherwise>
    <Action/>
</Otherwise>

```



```xml
<Variable name="" expression="">
</Variable>

<Warning name="">
</Warning>

<Notify type="" code="" severity="" title="">
</Notify>

<Insert select="">
    <Attribute name="" value=""/>
    <Node axis=""/>
</Insert>

```

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a>
